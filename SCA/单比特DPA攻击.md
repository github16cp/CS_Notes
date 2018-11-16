## 单比特DPA攻击实验
参考[DPAbook](http://dpabook.iaik.tugraz.at/onlinematerial/matlabscripts/index.htm)实验步骤

### 实验步骤
首先，读取能量轨迹

然后，针对每个明文输入，对每个猜测密钥计算中间值

最后，针对每个密钥计算差分能量轨迹

### 攻击实验代码
```Matlab
function [key_trace] = demo_dpa(workspace,first, last, method) % 单bit的DPA攻击

%DEMO_DPA is a demo to illustrate DPA attacks
%
% DESCRIPTION:
%
% demo_dpa(workspace, first, last, method) 
% performs a DPA with the specified method on some keys for some data
%    
% In the demo, the output of the AES SubBytes function is attacked. This
% demo works for the two sample Matlab workspace "WS1.mat" and "WS2.mat".
% Note that the power model is encoded in the demo. You need to look for
% "bitget" and "byte_Hamming_weight". Further note that the entire
% workspace is loaded to memory. This is no problem for WS1, but it might
% be nasty for machines with low memory, when working with WS2.
% 
% - workspace : the data that should be analyzed (traces, inputs)
%		       
% - first : keybyte to start with (1<=first <= 256)
% - last  : keybyte to end with (1<= first,last <= 256)
% - method: defines the statistical analysis (either 'kocher' or
% 'correlation')
%		
% RETURNVALUE:
%
% key_trace: a matrix that consist of the DPA traces for the keybytes.
% Although always a matrix with 256 rows is returned only the rows from
% 'first' to 'last' contain meaningful results.
%
% EXAMPLE:
%                                            
% keys = demo_dpa('WS1.zip',1,256,'correlation');


% Author: Elisabeth Oswald, 2.5.2004
% Last revision: 08.06.2006


% load data

disp('Reading in data ...');

load('-mat',workspace);
b = 1;
inputs = inputs(:,b);
% predict the SubBytes output: SubBytes(XOR(key,data))

disp('Predicting intermediate values ...');
[m,n] = size(traces);% m = 200, n =5000

key = [0:255];
after_sbox = zeros(m,256);% 中间值

for i = 1:m
    after_sbox(i,:) = SubBytes(bitxor(inputs(i),key)+1);% 加1,数组索引必须为正整数或逻辑值
end

key_trace = zeros(256,n);% 256*5000

if (strcmp(method,'kocher'))
    
    % predict the power consumption

    disp('Predicting the instantaneous power consumption ...');
    % 获取假设能量模型，并且取出依赖于中间值的某一个bit
    power_consumption = bitget(after_sbox,1);%返回每个元素最低第一bit位的值（1 or 0），和原来的矩阵维度相同
    %power_consumption = bitget(after_sbox,8); 这儿采用的是最低bit，即最低有效位，其他bit可不可以呢，经过实验
    % correlate the predicted power consumption with the real power 
    % consumption
    disp('Generating the difference traces ...');% 产生的差分能量轨迹

    for i = first:last % 对每一个猜测密钥
        % 这里按照中间值的其中一个bit对能量迹进行划分
        % 取出能量消耗矩阵每一列（对应i密钥）的行的索引，也就是明文索引，
        % 对应原来的能量轨迹的索引，取出这些依赖于这个bit == 1的轨迹
        % 取出这个中间值最高位等于1的轨迹和 - 最高位等于0的轨迹和
        
        key_trace(i,:) = sum(traces(find(power_consumption(:,i) == 1),:)) - sum(traces(find(power_consumption(:,i)==0),:));

    end

end

if (strcmp(method,'correlation'))

    % predict the power consumption

    disp('Predicting the instantaneous power consumption ...');
    power_consumption = byte_Hamming_weight(after_sbox+1);
    
    % correlate the predicted power consumption with the real power
    % consumption
    disp('Generating the correlation traces ...');

    chunksize=50;
    chunks=n/50;
    for i=first:last
        for j=1:chunks
            cmatrix= corrcoef([traces(:,1+(j-1)*chunksize:j*chunksize)  power_consumption(:,i)]);
            key_trace(i,1+(j-1)*chunksize:j*chunksize) =cmatrix(chunksize+1,1:chunksize);
            
        end
    end

end
```
### 实验结果
```Matlab
key_traces = demo_dpa('WS1.mat',1,256,'kocher');
show_plots(key_traces,1,256,1,800)  % 800代表着ylabel（-800，800）
```
可以看到在第44张图中获得了较为清晰的尖峰，也就是对应着差分能量轨迹矩阵的第44行，对应的猜测密钥为43

<p align="center">
    <img src="https://github.com/github16cp/CS_Notes/blob/master/SCA/one_bit_DPA.jpg" alt="Sample"  width="550" height="400">
</p>

在具体实验过程中，最低有效位的效果比较好，当取第4bit的时候（每个数用8bit表示，0-255）效果也很不错，为什么呢？尤其令我感到困惑的是，在选择最高有效位进行攻击的时候，差分结果也没有明显的尖峰，但理论上来说，最低有效位（LSB）和最高有效位（MSB）的影响应该是差不多的，但是差分结果尤其的差为什么呢？**这一个点**是不是也可以深入探究一下。
单比特DPA攻击是存在问题的，因为每个比特之间是存在关系的，并不是我们独立的认为的每个bit可以对计算过程独立地产生影响。
