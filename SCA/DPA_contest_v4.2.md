## Window平台 Matlab语言 针对DPA_contest_v4.2的学习测试
### 通信协议
攻击包装器（the attack wrapper）和攻击程序（attack program）之间的通信过程：attack program读取wrapper通过FIFO（FIFO类似于一个文件，用于wrapper和attack program之间的通信）发送来的能量轨迹，攻击程序然后通过另外一个FIFO发送结果给wrapper。

在这个过程中，首先先在windows命令提示符中启动wrapper，然后手动在matlab中启动attack program。

### 攻击案例
examples/v4_2/attack_windows.m，在这个文件里需要修改的是输入FIFO的名称、输出FIFO的名称、攻击的子密钥的数量
、攻击代码（共需要填写4项）

如果wrapper使用fork mode(Unix)，wrapper自己启动；windows上wrapper使用FIFO mode，wrapper会产生两个特别的文件，这个时候attack必须手动启动，而且必须打开这两个文件，在windows上`\\.\pipe\xxx_from_wrapper`只读模式，`\\.\pipe\xxx_to_wrapper`只写模式

接着，从wrapper中读数据，attack program从`\\.\pipe\xxx_from_wrapper`中读，发送数据`\\.\pipe\xxx_to_wrapper`，xxx表示fifo，即命令的最后一个参数

但是在具体实验的过程中，选择v4_2版本的数据集，即128bit的AES掩码方案的实现的能量轨迹，实验并不成功。

于是，改变数据集，也是很无奈啊，使用DPA_contestv4_rsm数据集，从官网上下载的0-9999一共1w条轨迹，在读取的时候只使用了0-5个（单单为了测试tools能不能用）

测试步骤如下：

1. 首先在windows命令提示符界面输入
```
D:\attack_wrapper-2.2.0>attack_wrapper -d DPA_contestv4_rsm -x dpav4_rsm_index -e v4_RSM fifo
```
`-d`：轨迹的所在目录

`-x`: index file

`-e`: 数据集版本

最后一个参数：`fifo`, 在windows中wrapper和attack的通信方式是fifo

2. 显示结果
```
D - Output filename = results (abort if exists)
D - FIFO mode
D - Base name for FIFOs = fifo
D - Compatibility mode (v2) = disabled
D - Traces will be read from directory DPA_contestv4_rsm
D - Using index file dpav4_rsm_index
D - We will check if traces are available
D - Offsets are not provided to the attack
I - Reading index file...
D - Total number of traces in the index file = 6
D - Total number of traces available = 6
D - Total number of keys in the index file = 1
D - Total number of keys available = 1
D - Key #00 (6cecc67f287d083deb8766f0738b36cf164ed9b246951090869d08285d2e193b): 6 traces available
D - Key # = 0
D - # of traces = 6
I - Preparing the results file...
I - FIFO Wrapper -> Attack: \\.\pipe\fifo_from_wrapper
I - FIFO Attack -> Wrapper: \\.\pipe\fifo_to_wrapper
I - Sending # of iterations (6)
I - The attack is ready!
```
**v4_2应该也是可行的，是不是因为解压了轨迹的原因**

3. matlab中命令行输入
```
attack_windows
```
4. 然后在命令行提示符界面看到以下结果
```
I - Trace #000000: Reading trace / Sending trace / Waiting for results / Saving results / Done (9.6 s) [                ]
I - Trace #000001: Reading trace / Sending trace / Waiting for results / Saving results / Done (9.1 s) [                ]
I - Trace #000002: Reading trace / Sending trace / Waiting for results / Saving results / Done (9.0 s) [                ]
I - Trace #000003: Reading trace / Sending trace / Waiting for results / Saving results / Done (9.2 s) [                ]
I - Trace #000004: Reading trace / Sending trace / Waiting for results / Saving results / Done (9.7 s) [                ]
I - Trace #000005: Reading trace / Sending trace / Waiting for results / Saving results / Done (10.1 s) [                ]
I - Closing the results file...
I - FIFOs closed
```
此时生成一个result文件，用记事本打开是乱码，这个时候就需要官网自带的结果分析工具对结果进行分析，这个分析工具用来计算不同的评价指标
5. 使用compute_results
```
D:\attack_wrapper-2.2.0>compute_results.exe results
I - Open file results
II - Compute result metrics
II - Writing result files
```
results文件的名字可以在开始指定，目录下多出了很多的文件，打开其中一个`results_global_success_rate.dat`，显示结果如下
```
# Trace_num Global_success_rate
0 0.000000
1 0.000000
2 0.000000
3 0.000000
4 0.000000
5 0.000000
```
分析对于v4_2错误的原因：轨迹文件解压之后，保持原来的文件名不变，即k00，trc.bz2文件不用解压缩，再次测试

测试结果：
```
D:\ML-SCA\SCA\DPA_traces\attack_wrapper-2.2.0>attack_wrapper -i 5 -d D:\ML-SCA\SCA\DPA_traces\DPA_contestv4_2 -x D:\ML-SCA\SCA\DPA_traces\dpav4_2_index -e v4_2 fifo
D - Output filename = results (abort if exists)
D - FIFO mode
D - Base name for FIFOs = fifo
D - Compatibility mode (v2) = disabled
D - Traces will be read from directory D:\ML-SCA\SCA\DPA_traces\DPA_contestv4_2
D - Using index file D:\ML-SCA\SCA\DPA_traces\dpav4_2_index
D - We will check if traces are available
D - Offsets/Shuffles are not provided to the attack
D - Samples are transfered as floats
I - Reading index file (v4_2)...
D - Total number of traces in the index file = 5
D - Total number of traces available = 5
D - Total number of keys in the index file = 1
D - Total number of keys available = 1
D - Key #00 (8249ceb658c71d41d7b734449629ab97): 5 traces available
D - Key # = 0
D - # of traces = 5
I - Preparing the results file...
I - FIFO Wrapper -> Attack: \\.\pipe\fifo_from_wrapper
I - FIFO Attack -> Wrapper: \\.\pipe\fifo_to_wrapper
I - Sending # of iterations (5)
I - The attack is ready!
I - Trace #000000: Reading trace / Sending trace / Waiting for results / Saving results / Done (251.9 s) [                ]
I - Trace #000001: Reading trace / Sending trace / Waiting for results / Saving results / Done (249.4 s) [                ]
I - Trace #000002: Reading trace / Sending trace / Waiting for results / Saving results / Done (249.6 s) [                ]
I - Trace #000003: Reading trace / Sending trace / Waiting for results / Saving results / Done (249.7 s) [                ]
I - Trace #000004: Reading trace / Sending trace / Waiting for results / Saving results / Done (1129.2 s) [                ]
I - Closing the results file...
I - FIFOs closed
```
此时显示可以成功读取能量轨迹

但是有一个问题，v4_2文件的读取速度明显比v4_rsm慢

-------
### AES128实现
基于RSM（旋转S盒掩码），选择的掩码值是公开的（16个），根据offset（0-15）确定掩码值，所以第一步就是恢复出掩码，也就是offset。

各位大佬们在各种传统方法上做的已经很深了，自己想要做出些，还是要深入钻研在方法或者方法组合上，找到一个突破点

现在已有的攻击：[参考论文](http://www.dpacontest.org/v4/data/v4_2/article_implem_dpav42.pdf)

分析一下下载的v4_2数据集的特征，查看[dpav4_2_index](http://www.dpacontest.org/v4/traces/v4_2/dpav4_2_index)文件
Example:
8249CEB658C71D41D7B734449629AB97 73136C16F1E0CE864A2A2C6C8400CF01 BDAA8B4BE13E13CD5250685B67443F84 AB5D4F761C28E039 1A9406F3B2857CED 05C229626F9D8B39 k00 DPACV42_000000.trc.bz2
> * 1st column: the AES-128 key (128 bits represented as 32 hexadecimal digits)
>* 2nd column: the plaintext (128 bits represented as 32 hexadecimal digits)
>* 3rd column: the ciphertext (128 bits represented as 32 hexadecimal digits)
> * 4th column: the Shuffle0 permutation (see the algorithm specifications, 16 x 1 hexadecimal digit)
> * 5th column: the Shuffle10 permutation (see the algorithm specifications, 16 x 1 hexadecimal digit) 
> * 6th column: the offsets (see the algorithm specifications, 16 x 1 hexadecimal digit)
> * 7th column: the name of the directory (below the top-level directory DPA_contestv4_2) where the trace is stored
> * 8th column: the name of the trace

此处的`k00`指的是子目录，不是密钥

### AES-256 RSM Reference Traces
-------
Example:

6cecc67f287d083deb8766f0738b36cf164ed9b246951090869d08285d2e193b 448ff4f8eae2cea393553e15fd00eca1 f71e9995e754e9f711b4027106a72788 8 00000 Z1Trace00000.trc.bz2

>* 1st column: the AES-256 key (256 bits represented as 64 hexadecimal digits)
>* 2nd column: the plaintext (128 bits represented as 32 hexadecimal digits)
>* 3rd column: the ciphertext (128 bits represented as 32 hexadecimal digits)
>* 4th column: the offset (see the AES-256 RSM specifications, 0-15 represented as 1 hexadecimal digit)
>* 5th column: the name of the directory (below the top-level directory DPA_contestv4_rsm) where the trace is stored
>* 6th column: the name of the trace

首先选取10条轨迹

10条轨迹的index file是
```
6cecc67f287d083deb8766f0738b36cf164ed9b246951090869d08285d2e193b 448ff4f8eae2cea393553e15fd00eca1 f71e9995e754e9f711b4027106a72788 8 00000 Z1Trace00000.trc.bz2
6cecc67f287d083deb8766f0738b36cf164ed9b246951090869d08285d2e193b d0edb7612c4dc8aa42358571649af40c f0fbbbb6e7d2befb7b947e9250fcd754 8 00000 Z1Trace00001.trc.bz2
6cecc67f287d083deb8766f0738b36cf164ed9b246951090869d08285d2e193b 7b7ab1b76d3db7a2008831a55590c827 41662fafb9a7fe2b29b5a31ecc590b60 b 00000 Z1Trace00002.trc.bz2
6cecc67f287d083deb8766f0738b36cf164ed9b246951090869d08285d2e193b c70ff17fda57839cd92872a65250f56c 19097cf5f18519a07d4a51c481961a95 5 00000 Z1Trace00003.trc.bz2
6cecc67f287d083deb8766f0738b36cf164ed9b246951090869d08285d2e193b ff3e730a1cb7dba0aea12ee257121f42 bc67f3dab2e90331f7b36169fc452a9e 4 00000 Z1Trace00004.trc.bz2
6cecc67f287d083deb8766f0738b36cf164ed9b246951090869d08285d2e193b 48448f4cdde30b43c9f18fd11c60084e 2b1532ff6f8901ef269e1394329fc9bb 3 00000 Z1Trace00005.trc.bz2
6cecc67f287d083deb8766f0738b36cf164ed9b246951090869d08285d2e193b 0998a9beea95bc011d6adc157079bd19 419aa3d597755de4c57846b7d692cb77 c 00000 Z1Trace00006.trc.bz2
6cecc67f287d083deb8766f0738b36cf164ed9b246951090869d08285d2e193b 126798e68ed1ba27010d2e811b7a445d 375a294098957d40d1ae39317cf88ae9 a 00000 Z1Trace00007.trc.bz2
6cecc67f287d083deb8766f0738b36cf164ed9b246951090869d08285d2e193b 05b3da69ba3958f9ef7540f3182b53f0 c3eb892a2dd505333dfe3fa6220935b3 d 00000 Z1Trace00008.trc.bz2
6cecc67f287d083deb8766f0738b36cf164ed9b246951090869d08285d2e193b 3392707787a58c9c92b5e2627e2ab7a3 9c0a243c95ae13db38317cd2127e6783 e 00000 Z1Trace00009.trc.bz2
```

mask set

{
    
    0x00, 0x0f, 0x36, 0x39, 0x53, 0x5c, 0x65, 0x6a, 
    0x95, 0x9a, 0xa3, 0xac, 0xc6, 0xc9, 0xf0, 0xff
    
}

实验过程中出现`Permission Denied`，将自己建的results文件夹删除后没有这个问题，或者文件不使用results。

目标实现SVM的攻击，距离目标还是好远好远啊
