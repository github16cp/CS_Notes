<!-- GFM-TOC -->
* [前言](#前言)
* [1. 二维数组中的查找](#1-二维数组中的查找)
* [2. 替换空格](#2-替换空格)
* [3. 从尾到头打印链表](#3-从尾到头打印链表)
* [4. 重建二叉树](#4-重建二叉树)
* [5. 用两个栈实现队列](#5-用两个栈实现队列)
* [6. 旋转数组的最小数字](#6-旋转数组的最小数字)
* [7. 斐波那契数列](#7-斐波那契数列)
* [8. 跳台阶](#8-跳台阶)
* [9. 变态跳台阶](#9-变态跳台阶)
* [10. 矩形覆盖](#10-矩形覆盖)
* [11. 二进制中1的个数](#11-二进制中1的个数)
* [12. 数值的整数次方](#12-数值的整数次方)
* [13. 调整数组顺序使奇数位于偶数前面](#13-调整数组顺序使奇数位于偶数前面)
* [14. 链表中倒数第k个结点](#14-链表中倒数第k个结点)
* [15. 反转链表](#15-反转链表)
* [16. 合并两个排序的链表](#16-合并两个排序的链表)
* [17. 树的子结构](#17-树的子结构)
* [18. 二叉树的镜像](#18-二叉树的镜像)
* [19. 顺时针打印矩阵](#19-顺时针打印矩阵)
* [20. 包含min函数的栈](#20-包含min函数的栈)
* [21. 栈的压入、弹出序列](#21-栈的压入、弹出序列)
* [22. 从上往下打印二叉树](#22-从上往下打印二叉树)
* [23. 二叉搜索树的后序遍历序列](#23-二叉搜索树的后序遍历序列)
* [24. 二叉树中和为某一值的路径](#24-二叉树中和为某一值的路径)
* [25. 复制链表的复制](#25-复制链表的复制)
* [26. 二叉搜索树与双向链表](#26-二叉搜索树与双向链表)
* [27. 字符串的排列](#27-字符串的排列)
* [28. 数组中出现次数超过一半的数字](#28-数组中出现次数超过一半的数字)
* [附. 快速排序算法的实现](#附-快速排序算法的实现)
* [29. 最小的K个数](#29-最小的K个数)
* [附. 迭代器](#附-迭代器)
* [附. 二分查找下标问题](#附-二分查找下标问题)
* [30. 连续子数组的最大和](#30-连续子数组的最大和)
* [31. 整数中1出现的次数](#31-整数中1出现的次数)
* [32. 把数组排成最小的数](#32-把数组排成最小的数)
* [33. 丑数](#33-丑数)
* [34. 第一个只出现一次的字符](#34-第一个只出现一次的字符)
* [35. 数组中的逆序对](#35-数组中的逆序对)
* [36. 两个链表中的第一个公共结点](#36-两个链表中的第一个公共结点)
* [37. 数字在排序数组中出现的次数](#37-数字在排序数组中出现的次数)
* [38. 二叉树的深度](#38-二叉树的深度)
* [39. 平衡二叉树](#39-平衡二叉树)
* [40. 数组中只出现一次的数字](#40-数组中只出现一次的数字)
* [41. 和为S的连续正数序列](#41-和为S的连续正数序列)
* [42. 和为S的两个数字](#42-和为S的两个数字)
* [43. 左旋转字符串](#43-左旋转字符串)
* [44. 翻转单词顺序列](#44-翻转单词顺序列)
* [45. 扑克牌顺子](#45-扑克牌顺子)
* [46. 圆圈中最后剩下的数](#46-圆圈中最后剩下的数)
* [47. 求1+2+3+...+n](#47-求1+2+3+...+n)
* [48. 不用加减乘除做加法](#48-不用加减乘除做加法)
* [49. 把字符串转换成整数](#49-把字符串转换成整数)
* [50. 数组中重复的数字](#50-数组中重复的数字)
* [51. 构建乘积数组](#51-构建乘积数组)
* [52. 正则表达式匹配](#52-正则表达式匹配)
* [53. 表示数值的字符串](#53-表示数值的字符串)
* [54. 字符流中第一个不重复的字符](#54-字符流中第一个不重复的字符)
* [55. 链表中环的入口结点](#55-链表中环的入口结点)
* [56. 删除链表中重复的结点](#56-删除链表中重复的结点)
* [57. 二叉树的下一个结点](#57-二叉树的下一个结点)
* [58. 对称的二叉树](#58-对称的二叉树)
* [59. 按之字形顺序打印二叉树](#59-按之字形顺序打印二叉树)
* [60. 把二叉树打印成多行](#60-把二叉树打印成多行)
* [61. 序列化二叉树](#61-序列化二叉树)
* [62. 二叉搜索树的第k个结点](#62-二叉搜索树的第k个结点)
* [63. 数据流中的中位数](#63-数据流中的中位数)
* [64. 滑动窗口的最大值](#64-滑动窗口的最大值)
* [65. 矩阵中的路径](#65-矩阵中的路径)
* [66. 机器人的运动范围](#66-机器人的运动范围)
* [67. 剪绳子](#67-剪绳子)
<!-- GFM-TOC -->

# 前言

`剑指Offer`

`C++ Primer`

`数据结构`

`算法导论`

`无他，唯手熟尔`

# 1. 二维数组中的查找

在一个二维数组中（每个一维数组的长度相同），每一行都按照从左到右递增的顺序排序，每一列都按照从上到下递增的顺序排序。请完成一个函数，输入这样的一个二维数组和一个整数，判断数组中是否含有该整数。

```C++
class Solution {
public:
    bool Find(int target, vector<vector<int> > array) {
        int row = (int)array.size();
        int col = (int)array[0].size();
        
        if(row == 0 || col == 0)
            return false;
        
        if(target < array[0][0] || target > array[row-1][col-1])
            return false;
        
        for(int i=0;i<row;i++){
            int l = 0,r = col - 1,m;
            while(l <= r){
                m = (l+r)/2;
                if(target == array[i][m])
                    return true;
                else if(target < array[i][m])
                    r = m - 1;
                else
                    l = m + 1;
            }
        }
        
        return false;
    }
};
```

# 2. 替换空格

请实现一个函数，将一个字符串中的每个空格替换成“%20”。例如，当字符串为We Are Happy.则经过替换之后的字符串为We%20Are%20Happy。

```C++
class Solution {
public:
	void replaceSpace(char *str, int length) {
		int count = 0;
		for (int i = 0; i < length; i++) {
			if (str[i] == ' ')
				count++;
		}

		for (int i = length - 1; i >= 0; i--) {
			if (str[i] != ' ') {
				str[i + 2*count] = str[i];
			}
			else {
				count--;
				str[i + 2*count] = '%';
				str[i + 2 * count + 1] = '2';
				str[i + 2 * count + 2] = '0';
			}
		}
	}
};
```

# 3. 从尾到头打印链表

输入一个链表，按链表值从尾到头的顺序返回一个ArrayList。

```C++
/**
*  struct ListNode {
*        int val;
*        struct ListNode *next;
*        ListNode(int x) :
*              val(x), next(NULL) {
*        }
*  };
*/
class Solution {
public:
	vector<int> printListFromTailToHead(ListNode* head) {
		vector<int> list;
		if (head != NULL) {
			list.insert(list.begin(), head->val);
			if (head->next != NULL) {
				vector<int> tempVal = printListFromTailToHead(head->next);
				if (tempVal.size() > 0)
					list.insert(list.begin(), tempVal.begin(), tempVal.end());
			}
		}
		return list;
	}
};
```

# 4. 重建二叉树

输入某二叉树的前序遍历和中序遍历的结果，请重建出该二叉树。假设输入的前序遍历和中序遍历的结果中都不含重复的数字。例如输入前序遍历序列{1,2,4,7,3,5,6,8}和中序遍历序列{4,7,2,1,5,3,8,6}，则重建二叉树并返回。

```C++
#include<iostream>
#include<vector>
#include<queue>
using namespace std;

/**
* Definition for binary tree */
struct TreeNode {
	int val;
	TreeNode *left;
	TreeNode *right;
	TreeNode(int x) : val(x), left(NULL), right(NULL) {}
};

class Solution {
public:
	TreeNode * reConstructBinaryTree(vector<int> pre, vector<int> vin) {
		int vin_len = vin.size();
		if (vin_len == 0)
			return NULL;

		vector<int> pre_left, pre_right, vin_left, vin_right;

		TreeNode *root = new TreeNode(pre[0]);

		int root_index = 0;
		for (int i = 0; i < vin_len; i++) {
			if (vin[i] == root->val) {
				root_index = i;
				break;
			}
		}
		//构建左子树
		for (int i = 0; i < root_index; i++) {
			vin_left.push_back(vin[i]);
			pre_left.push_back(pre[i + 1]);
		}
		//构建右子树
		for (int i = root_index + 1; i < vin_len; i++) {
			vin_right.push_back(vin[i]);
			pre_right.push_back(pre[i]);
		}
		root->left = reConstructBinaryTree(pre_left, vin_left);
		root->right = reConstructBinaryTree(pre_right, vin_right);
		return root;
	}

	vector<int> PrintFromTopToBottom(TreeNode* root) {
		TreeNode* fr;
		if (root == NULL) {
			return result;
		}
		que.push(root);
		while (!que.empty()) {
			fr = que.front();
			result.push_back(fr->val);
			if (fr->left != NULL) {
				que.push(fr->left);
			}
			if (fr->right != NULL) {
				que.push(fr->right);
			}
			que.pop();
		}
		return result;
	}
private:
	vector<int> result;
	queue<TreeNode*> que;

};

int main() {
	Solution s;
	int a[8] = { 1,2,4,7,3,5,6,8 };
	int b[8] = { 4,7,2,1,5,3,8,6 };
	vector<int> pre;
	pre.insert(pre.begin(), a, a + 8);
	vector<int> vin;
	vin.insert(vin.begin(), b, b + 8);
	TreeNode *root = s.reConstructBinaryTree(pre, vin);
	vector<int> result = s.PrintFromTopToBottom(root);
	vector<int>::iterator it;
	for (it = result.begin(); it != result.end(); ++it) {
		cout << *it << endl;
	}

	system("pause");
	return 0;
}

/*
*                   1
*                 *    *
*              2          3
*            *           *   *
*          4            5      6
*         *
*       8
*/
```

# 5. 用两个栈实现队列

```C++
/* 题目：用两个栈实现队列
* 题目描述
* 用两个栈来实现一个队列，完成队列的Push和Pop操作。 队列中的元素为int类型。
*/

#include<iostream>
#include<stack>
using namespace std;

class Solution
{
public:
	void push(int node) {
		stack1.push(node);
	}

	int pop() {
		int res = 0;
		if (stack2.size() > 0) {
			res = stack2.top();
			stack2.pop();
		}
		else if (stack1.size() > 0) {
			while (stack1.size() > 0) {
				stack2.push(stack1.top());
				stack1.pop();
			}
			res = stack2.top();
			stack2.pop();
		}
		return res;
	}

private:
	stack<int> stack1;
	stack<int> stack2;
};

int main() {
	Solution s;
	s.push(5);
	s.push(6);
	s.pop();
	system("pause");
	return 0;
}
```

# 6. 旋转数组的最小数字

```C++
/* 题目：旋转数组的最小数字
* 题目描述
* 把一个数组最开始的若干个元素搬到数组的末尾，我们称之为数组的旋转。
* 输入一个非减排序的数组的一个旋转，输出旋转数组的最小元素。
* 例如数组{3,4,5,1,2}为{1,2,3,4,5}的一个旋转，该数组的最小值为1。
* NOTE：给出的所有元素都大于0，若数组大小为0，请返回0。
*/

#include<iostream>
#include<vector>
using namespace std;

class Solution {
public:
	int minNumberInRotateArray(vector<int> rotateArray) {
		int size = rotateArray.size();
		if (size == 0) {
			return 0;
		}
		int left = 0, right = size - 1;
		int mid = 0;
		while (rotateArray[left] >= rotateArray[right]) {
			if (right - left == 1) {
				mid = right;
				break;
			}
			mid = (left + right) / 2;
			if (rotateArray[left] == rotateArray[right] && rotateArray[left] == rotateArray[mid]) {
				return MinNumber(rotateArray, left, right);
			}
			if (rotateArray[mid] >= rotateArray[left]) {
				left = mid;
			}
			else {
				right = mid;
			}
		}
		return rotateArray[mid];
	}
private:
	int MinNumber(vector<int> &num, int left, int right) {
		int res = num[left];
		for (int i = left + 1; i < right; i++) {
			if (num[i] < res) {
				res = num[i];
			}
		}
		return res;
	}
};

int main() {
	Solution s;
	vector<int> num = { 4,5,6,7,1,2,3 };
	cout << s.minNumberInRotateArray(num) << endl;
	system("pause");
	return 0;
}
```

# 7. 斐波那契数列

```C++
/* 题目：斐波那契数列
* 题目描述
* 大家都知道斐波那契数列，现在要求输入一个整数n，请你输出斐波那契数列的第n项（从0开始，第0项为0）。n<=39
*/

#include<iostream>
using namespace std;

class Solution {
public:
	/*int Fibonacci(int n) {
	if (n < 0)
	return -1;
	else if (n == 0)
	return 0;
	else if (n == 1)
	return 1;
	else
	return Fibonacci(n - 1) + Fibonacci(n - 2);
	}*/ //递归时间消耗太大
	int Fibonacci(int n) {
		if (n < 0)
			return -1;
		else if (n == 0)
			return 0;
		else if (n == 1 || n == 2)
			return 1;
		else {
			int first = 1, second = 1, temp;
			for (int i = 2; i < n; i++) {
				temp = first + second;
				first = second;
				second = temp;
			}
			return temp;
		}
	}
};

int main() {
	Solution s;
	cout << s.Fibonacci(5) << endl;
	system("pause");
	return 0;
}
```

# 8. 跳台阶

```C++
/* 题目：跳台阶
* 题目描述
* 一只青蛙一次可以跳上1级台阶，也可以跳上2级。
* 求该青蛙跳上一个n级的台阶总共有多少种跳法（先后次序不同算不同的结果）。
*/

/* 两种跳法:
1. 第一次跳是1级，那么剩下的是n-1个台阶，跳法是f(n-1);
2. 第一次跳是2级，那么剩下的是n-2个台阶，跳法是f(n-2);
3. 总跳法是f(n) = f(n-1) + f(n-2);
f(1) = 1; f(2) = 2; f(3) = 3;Fibonacci数列
*/

/* 
* 递归方法对时间和空间的消耗比较大。
*/

#include<iostream>
using namespace std;

class Solution {
public:
	int jumpFloor(int number) {
		/*if (number == 1) {
			return 1;
		}
		else if (number == 2) {
			return 2;
		}
		else {
			return jumpFloor(number - 1) + jumpFloor(number - 2);
		}*/
		if (number < 1) {
			return 0;
		}
		else if (number == 1) {
			return 1;
		}
		else if(number == 2){
			return 2;
		}
		else {
			int first = 1, second = 2, third;
			for (int i = 3; i <= number; i++) {
				third = first + second;
				first = second;
				second = third;
			}
			return third;
		}
	}
};

int main() {
	Solution s;
	cout << s.jumpFloor(5) << endl;
	system("pause");
	return 0;
}
```

# 9. 变态跳台阶

```C++
#include<iostream>
using namespace std;

/* 题目：变态跳台阶
* 题目描述
* 一只青蛙一次可以跳上1级台阶，也可以跳上2级……它也可以跳上n级。求该青蛙跳上一个n级的台阶总共有多少种跳法。
*/

/* 两种跳法:
1. 第一次跳是1级，那么剩下的是n-1个台阶，跳法是f(n-1);
2. 第一次跳是2级，那么剩下的是n-2个台阶，跳法是f(n-2);
3. 第一次跳是n级，那么剩下的是0个台阶，跳法是f(0);
总跳法是f(n) = f(n-1) + f(n-2) + ... + f(1) + f(0);
f(n - 1) = f(n - 2) + ... + f(0);
f(n) = f(n-1)+ f(n-1) = 2*f(n-1);
f(0) = 1;
f(1) = 1;
f(2) = 2;
*/

class Solution {
public:
	int jumpFloorII(int number) {
		if (number == 0 || number == 1) {
			return 1;
		}
		else if (number > 0) {
			int res = 1;
			for (int i = 2; i <= number; i++) {
				res = 2 * res;
			}
			return res;
		}
		else {
			return 0;
		}
	}
};

int main() {
	Solution s;
	cout << s.jumpFloorII(5) << endl;
	system("pause");
	return 0;
}
```

# 10. 矩形覆盖

```C++
#include<iostream>
using namespace std;

/* 题目：矩形覆盖
* 题目描述
* 我们可以用2*1的小矩形横着或者竖着去覆盖更大的矩形。
* 请问用n个2*1的小矩形无重叠地覆盖一个2*n的大矩形，总共有多少种方法？
*/

/* 
1. 当n=1时，只有一种方法；
2. 当n=2时，有两种方法；
第一块横着放，f(n-2)种放法；
第一块竖着放，f(n-1)种放法。
f(n) = f(n-1) + f(n-2);
*/

class Solution {
public:
	int rectCover(int number) {
		if (number < 1) {
			return 0;
		}
		else if (number == 1) {
			return 1;
		}
		else if (number == 2) {
			return 2;
		}
		else {
			int first = 1, second = 2, third;
			for (int i = 3; i <= number; i++) {
				third = first + second;
				first = second;
				second = third;
			}
			return third;
		}

	}
};

int main() {
	Solution s;
	cout << s.rectCover(4) << endl;
	system("pause");
	return 0;
}
```

# 11. 二进制中1的个数

```C++
#include<iostream>
using namespace std;

/* 题目：二进制中1的个数
* 题目描述
* 输入一个整数，输出该数二进制表示中1的个数。其中负数用补码表示。
*/

/* 题解
* 一个整数：0，正数，负数
* 这个数转换为2进制表示
* 负数怎么转换为2进制表示呢？

*********
* 从n的2进制形式的最右边开始判断是不是1
* 该解法如果输入时负数会陷入死循环，因为负数右移时，在最高位补得是1,
* 本题最终目的是求1的个数，那么会有无数个1了。
**********
* 用1（1自身左移运算，其实后来就不是1了）和n的每位进行位与，来判断1的个数
*/



class Solution {
public:
	int  NumberOf1(int n) {
		/*int count = 0;
		int flag = 1;
		while (flag != 0) {//停止条件 flag = 0，位数移动完毕
			if ((n & flag) != 0) {
				count++;				
			}
			flag = flag << 1;
		}
		return count;	*/
		int count = 0;
		while (n != 0) {
			count++;
			n = (n - 1) & n;
		}
		return count;
		
	}
};

int main() {
	Solution s;
	cout << s.NumberOf1(10) << endl;
	system("pause");
	return 0;
}
```

# 12. 数值的整数次方

```C++
#include<iostream>
using namespace std;

/* 题目：数值的整数次方
* 题目描述
* 给定一个double类型的浮点数base和int类型的整数exponent。求base的exponent次方。
* 考察点：代码的完整性
*/

/* 题解
* 底数base，指数exponent
* 指数为正，为0，为负三种情况
* 指数为正时,指数值为1时返回base，指数值大于1时的处理：
* 递归的方法，为偶数时，指数对半分；为奇数时，exponent/2，exponent/2+1

* 非递归方法，平方乘算法
*/

class Solution {
public:
	double Power(double base, int exponent) {
		/*if (exponent > 0) {
			if (exponent == 1) {
				return base;
			}
			else {
				if (exponent % 2 == 0) {
					return Power(base, exponent / 2) * Power(base, exponent / 2);
				}
				else {
					return Power(base, exponent / 2) * Power(base, exponent / 2 + 1);
				}
			}
		}
		else if (exponent == 0) {
			return 1;
		}
		else {
			return 1 / Power(base, 0 - exponent);
		}*/

		/*double res = 1, currentValue = base;
		int n = exponent;
		if (exponent > 0) {
			n = exponent;
		}
		else if (exponent < 0) {
			if (base == 0) {
				cout << "base cannot be zero!" << endl;
			}
			n = 0 - exponent;
		}
		else {
			return base;
		}
		while (n != 0) {
			if ((n & 1) != 0) {
				res *= currentValue;
			}
			currentValue *= currentValue;
			n >>= 1;
		}
		return res = exponent >= 0 ? res : (1 / res);*/
		return pow(base,exponent);
	}
};

int main() {
	Solution s;
	cout << s.Power(10,2) << endl;
	system("pause");
	return 0;
}
```

# 13. 调整数组顺序使奇数位于偶数前面

```C++
#include<iostream>
#include<vector>
using namespace std;

/* 题目：调整数组顺序使奇数位于偶数前面
* 题目描述
* 输入一个整数数组，实现一个函数来调整该数组中数字的顺序，
* 使得所有的奇数位于数组的前半部分，所有的偶数位于数组的后半部分，
* 并保证奇数和奇数，偶数和偶数之间的相对位置不变。
*/

/* 题解
* 空间换取时间
****************************
* 或者可以采取另外一种插排的方式
* 将偶数删除再添加到最后，erase
*/

class Solution {
public:
	void reOrderArray(vector<int> &array) {
		int size = (int)array.size();//返回size_t类型,int强制转换一下
		if (size == 0) {
			return ;
		}
		vector<int> oddArray;
		vector<int> evenArray;
		for (int i = 0; i < size; i++) {
			if (array[i] % 2 == 1) {
				oddArray.push_back(array[i]);
			}
			else {
				evenArray.push_back(array[i]);
			}
		}
		for (int i = 0; i < size; i++) {
			array.pop_back();
		}
		for (int i = 0; i < (int)oddArray.size(); i++) {
			array.push_back(oddArray[i]);
		}
		for (int i = 0; i < (int)evenArray.size(); i++) {
			array.push_back(evenArray[i]);
		}

		/*for (int i = 0; i < size; i++) {
			cout << array[i] << endl;
		}*/
	}
};
int main() {
	Solution s;
	vector<int> num = { 1,2,3,4,5,6 };
	s.reOrderArray(num);
	system("pause");
	return 0;
}
```

# 14. 链表中倒数第k个结点

[常见链表操作](https://github.com/selfconzrr/LinkedList_learning)

```C++
#include<iostream>
using namespace std;

/* 题目：链表中倒数第k个结点
* 题目描述
* 输入一个链表，输出该链表中倒数第k个结点。
*/

/* 题解
* 我的思路：遍历统计链表中结点的个数，然后根据个数再从前往后找所要寻找的结点
* 大神思路：两个指针，制造一个K长度的尺子，把尺子从头往后移动，
* 当尺子的右端与链表的末尾对齐的时候，尺子的左端所在的结点就是倒数第k个结点。
* 优点：遍历次数减少，刚好遍历k个，相对于全部遍历再加一部分遍历优化很多。
*/

/*
* 双指针定位
*/

struct ListNode {
	int val;
	struct ListNode *next;
	ListNode(int x) :val(x), next(NULL) {}
};

/*class Solution {
public:
	ListNode * FindKthToTail(ListNode* pListHead, unsigned int k) {
		if (pListHead == NULL) {
			return NULL;
		}
		ListNode *res = pListHead;
		ListNode *tmp = pListHead;
		unsigned int n = 0;
		while (tmp != NULL) {
			n++;
			tmp = tmp->next;
		}
		if (k > n) {
			return NULL;
		}
		for (unsigned int i = 1; i < n - k + 1;i++) {
			res = res->next;
		}
		return res;
	}
};*/

class Solution {
public:
	ListNode * FindKthToTail(ListNode* pListHead, unsigned int k) {
		if (pListHead == NULL) 
			return pListHead;
		if (k == 0) 
			return NULL;
		ListNode* kth = NULL, *end = pListHead;
		int count = 1;
		while (end != NULL) {
			if (count++ == k) {
				kth = pListHead;
			}
			else if (count>k) {
				kth = kth->next;
			}
			end = end->next;
		}
		return kth;
	}
};

int main() {
	Solution s;
	ListNode *res = NULL;
	s.FindKthToTail(res,2);
	system("pause");
	return 0;
}
```

# 15. 反转链表

```C++
#include<iostream>
#include<stack>
using namespace std;

/* 题目：反转链表
* 题目描述
* 输入一个链表，反转链表后，输出新链表的表头。
*/

/* 题解
* 利用stack进行链表反转，将原来链表依次压入栈，然后取出。
* 3个指针
* 递归
*/

/*链表初始化
* 要改变一下关于链表的思考方向。
* 即：
* 1、不要用初始化数组或结构的方式去处理链表；
* 2、链表的每一个节点要用一个子程序进行动态创建，同时赋值；
* 3、删除链表中的节点时，要注意回收内存；
*/

struct ListNode {
	int val;
	struct ListNode *next;
	ListNode(int x) :val(x), next(NULL) {}
};

class Solution {
public:
	/*ListNode * ReverseList(ListNode* pHead) {		
 		if (pHead == NULL || pHead->next == NULL) {
			return pHead;
		}
		stack<ListNode *> s;
		ListNode *p = pHead;
		while (p->next != NULL) {
			s.push(p);
			p = p->next;
		}
		ListNode *head = p;
		while (!s.empty()) {			
			p->next = s.top();						
			p = p->next;
			s.pop();
		}
		p->next = NULL;
		return head;
	}*/
	ListNode* ReverseList(ListNode* pHead) {

		if (pHead == NULL) {
			return pHead;
		}
		ListNode* pre = NULL;
		ListNode* cur = pHead;
		ListNode* nxt = NULL;
		while (cur != NULL) {
			nxt = cur->next;
			cur->next = pre;
			if (nxt == NULL) {
				break;
			}
			pre = cur;
			cur = nxt;
		}
		return cur;
	}
};

/*class Solution {
public:
	ListNode * ReverseList(ListNode* pHead) {
		//如果链表为空或者链表中只有一个元素
		if (pHead == NULL || pHead->next == NULL) return pHead;

		//先反转后面的链表，走到链表的末端结点
		ListNode* pReverseNode = ReverseList(pHead->next);

		//再将当前节点设置为后面节点的后续节点
		pHead->next->next = pHead;
		pHead->next = NULL;

		return pReverseNode;

	}
};*/

//尾插法建立单链表
ListNode * Creat_LinkList_R()
{
	int x;
	ListNode *head, *p, *tail;                    //tail是尾指针
	head = (ListNode*)malloc(sizeof(ListNode));
	if (head == NULL)
		return head;
	head->next = NULL;
	tail = head;                                  //一开始尾指针指向头指针的位置
	cout << "请输入要录入的数以0结束" << endl;
	cin >> x;
	head->val = x;
	while ((cin>>x) && (x != 0))
	{
		p = (ListNode*)malloc(sizeof(ListNode));
		if (p == NULL)
			return head;
		p->val = x;
		tail->next = p;                          //将p插入到尾节点的后面
		tail = p;                                //修改尾节点的指向
		tail->next = NULL;                       //将尾节点的指针域修改为空
	}
	return head;
}


int main() {
	Solution s;
	ListNode * res, *newList;
	res = Creat_LinkList_R();

	/*while (res != NULL) {		
		cout << res->val << endl;	
		res = res->next;
	}*/

	newList = s.ReverseList(res);

	while (newList != NULL) {
		cout << newList->val << endl;
		newList = newList->next;
	}

	system("pause");
	return 0;
}
```

# 16. 合并两个排序的链表
```C++
#include<iostream>
#include<stack>
using namespace std;

/* 题目：合并两个排序的链表
* 题目描述
* 输入两个单调递增的链表，输出两个链表合成后的链表，当然我们需要合成后的链表满足单调不减规则。
*/

/* 题解
* 1. 非递归方法，依次比较，O(N)的时间复杂度
* 2. 递归方法
*/

struct ListNode {
	int val;
	struct ListNode *next;
	ListNode(int x) :val(x), next(NULL) {}
};

class Solution {
public:
	ListNode * Merge(ListNode* pHead1, ListNode* pHead2)
	{
		if (pHead1 == NULL) {
			return pHead2;
		}
		else if(pHead2 == NULL){
			return pHead1;
		}
		else {
			ListNode * newList;
			if (pHead1->val <= pHead2->val) {
				newList = pHead1;
				newList->next = Merge(pHead1->next,pHead2);
			}
			else {
				newList = pHead2;
				newList->next = Merge(pHead1, pHead2->next);
			}
			return newList;
		}
	}
};


//尾插法建立单链表
ListNode * Creat_LinkList_R()
{
	int x;
	ListNode *head, *p, *tail;                    //tail是尾指针
	head = (ListNode*)malloc(sizeof(ListNode));
	if (head == NULL)
		return head;
	head->next = NULL;
	tail = head;                                  //一开始尾指针指向头指针的位置
	cout << "请输入要录入的数以0结束" << endl;
	cin >> x;
	head->val = x;
	while ((cin >> x) && (x != 0))
	{
		p = (ListNode*)malloc(sizeof(ListNode));
		if (p == NULL)
			return head;
		p->val = x;
		tail->next = p;                          //将p插入到尾节点的后面
		tail = p;                                //修改尾节点的指向
		tail->next = NULL;                       //将尾节点的指针域修改为空
	}
	return head;
}

int main() {
	Solution s;
	ListNode *list1, *list2, *newList;
	list1 = Creat_LinkList_R();
	list2 = Creat_LinkList_R();

	/*while (res != NULL) {
	cout << res->val << endl;
	res = res->next;
	}*/

	newList = s.Merge(list1, list2);

	while (newList != NULL) {
		cout << newList->val << endl;
		newList = newList->next;
	}

	system("pause");
	return 0;
}


```

# 17. 树的子结构

```C++
#include<iostream>
#include<queue>
using namespace std;

/* 题目：树的子结构
* 题目描述
* 输入两棵二叉树A，B，判断B是不是A的子结构。（ps：我们约定空树不是任意一个树的子结构）
*/

/* 题解
* 递归
*/


struct TreeNode {
	int val;
	struct TreeNode *left;
	struct TreeNode *right;
	TreeNode(int x) :val(x), left(NULL), right(NULL) {}
};


class Solution {
public:
	bool HasSubtree(TreeNode* pRoot1, TreeNode* pRoot2)
	{
		if (!pRoot1)
			return false;
		if (!pRoot2)
			return false;
		return ( doesTree1HasTree2(pRoot1, pRoot2) || HasSubtree(pRoot1->left, pRoot2) || HasSubtree(pRoot1->right, pRoot2) );
	}
	bool doesTree1HasTree2(TreeNode* tree1, TreeNode* tree2) {
		if (!tree2) //tree2判断在前
			return true;
		if (!tree1)
			return false;
		if (tree1->val != tree2->val)
			return false;
		return (doesTree1HasTree2(tree1->left, tree2->left) && doesTree1HasTree2(tree1->right, tree2->right) );//这儿不应该递归调用HasSubtree
	}
};

TreeNode* initBTree(int elements[], int size)
{
	if (size < 1)
	{
		return NULL;
	}
	//动态申请size大小的指针数组
	TreeNode **nodes = new TreeNode*[size];
	//将int数据转换为TreeNode节点
	for (int i = 0; i < size; i++)
	{
		if (elements[i] == 0)
		{
			nodes[i] = NULL;
		}
		else
		{
			nodes[i] = new TreeNode(elements[i]);
		}
	}
	queue<TreeNode*> nodeQueue;
	nodeQueue.push(nodes[0]);

	TreeNode *node;
	int index = 1;
	while (index < size)
	{
		node = nodeQueue.front();
		nodeQueue.pop();
		nodeQueue.push(nodes[index++]);
		node->left = nodeQueue.back();
		nodeQueue.push(nodes[index++]);
		node->right = nodeQueue.back();
	}
	return nodes[0];
}

int main() {
	Solution s;
	int nums[] = { 8,8,7,9,2,0,0,0,0,4,7};
	TreeNode *tree1 = initBTree(nums, 11);
	int nums2[] = { 8,9,2};
	TreeNode *tree2 = initBTree(nums2, 3);
	cout << s.HasSubtree(tree1, tree2) << endl;
	system("pause");
	return 0;
}
```

# 18. 二叉树的镜像

```C++
#include<iostream>
#include<queue>
using namespace std;

/* 题目：二叉树的镜像
* 题目描述
* 操作给定的二叉树，将其变换为源二叉树的镜像。
*/

/* 题解
* 递归
*/


struct TreeNode {
	int val;
	struct TreeNode *left;
	struct TreeNode *right;
	TreeNode(int x) :val(x), left(NULL), right(NULL) {}
};


class Solution {
public:
	void Mirror(TreeNode *pRoot) {
		if (!pRoot)
			return ;
		TreeNode * tmp;
		tmp = pRoot->right;
		pRoot->right = pRoot->left;
		pRoot->left = tmp;
		Mirror(pRoot->left);
		Mirror(pRoot->right);
	}
};

TreeNode* initBTree(int elements[], int size)
{
	if (size < 1)
	{
		return NULL;
	}
	//动态申请size大小的指针数组
	TreeNode **nodes = new TreeNode*[size];
	//将int数据转换为TreeNode节点
	for (int i = 0; i < size; i++)
	{
		if (elements[i] == 0)
		{
			nodes[i] = NULL;
		}
		else
		{
			nodes[i] = new TreeNode(elements[i]);
		}
	}
	queue<TreeNode*> nodeQueue;
	nodeQueue.push(nodes[0]);

	TreeNode *node;
	int index = 1;
	while (index < size)
	{
		node = nodeQueue.front();
		nodeQueue.pop();
		nodeQueue.push(nodes[index++]);
		node->left = nodeQueue.back();
		nodeQueue.push(nodes[index++]);
		node->right = nodeQueue.back();
	}
	return nodes[0];
}

void preOrder(TreeNode *root, vector<int> &result)
{
	if (root)
	{
		result.push_back(root->val);
		preOrder(root->left, result);
		preOrder(root->right, result);
	}
}

void traverse(vector<int> nums)
{
	vector<int>::size_type size = nums.size();
	for (size_t i = 0; i < size; i++)
	{
		cout << nums[i] << ' ';
	}
	cout << endl;
}

int main() {
	Solution s;
	vector<int> preResult;
	vector<int> preResult2;
	int nums[] = { 8,6,10,5,7,9,11};
	TreeNode *tree1 = initBTree(nums, 7);
	preOrder(tree1, preResult);
	cout << "前序遍历的结果：" << '\n';
	traverse(preResult);
	s.Mirror(tree1);
	preOrder(tree1, preResult2);
	cout << "镜像的结果：" << '\n';
	traverse(preResult2);
	system("pause");
	return 0;
}
```

# 19. 顺时针打印矩阵

```C++
#include<iostream>
#include<vector>
using namespace std;

/* 题目：顺时针打印矩阵
* 题目描述
* 输入一个矩阵，按照从外向里以顺时针的顺序依次打印出每一个数字，
* 例如，如果输入如下4 X 4矩阵： 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 
* 则依次打印出数字1,2,3,4,8,12,16,15,14,13,9,5,6,7,11,10.
*/

/* 题解
* 设置左右上下四个标识符，每一圈标识符改变
*/

class Solution {
public:
	vector<int> printMatrix(vector<vector<int> > matrix) {
		vector<int> res;
		int size_row = (int)matrix.size();
		int size_col = (int)matrix[0].size();
		int left = 0, right = size_col - 1, top = 0, btm = size_row - 1;
		while (left <= right && top <= btm) {
			for (int i = left; i <= right; i++) {
				res.push_back(matrix[top][i]);
			}
			if (top < btm) {
				for (int i = top + 1; i <= btm; i++) {
					res.push_back(matrix[i][right]);
				}
			}
			if (left < right && top < btm ) {
				for (int i = right - 1; i >= left; i--) {
					res.push_back(matrix[btm][i]);
				}
			}
			if (top < btm && left < right) {
				for (int i = btm - 1; i > top; i--) {
					res.push_back(matrix[i][left]);
				}
			}
			left++; right--; top++; btm--;
		}
		int size = res.size();
		for (int i = 0; i < size; i++) {
			cout << res[i] << " ";
		}
		cout << endl;
		return res;
	}
};

int main() {
	Solution s;
	vector<vector<int> > matirx(1);
	int num = 1;
	for (int i = 0; i < matirx.size(); ++i) {
		for (int j = 0; j < 5; ++j) {
			matirx[i].push_back(num);
			num++;
			cout << matirx[i][j] << " ";
		}
	}
	cout << endl;
	s.printMatrix(matirx);
	system("pause");
	return 0;
}
```

# 20. 包含min函数的栈

```C++
#include<iostream>
#include<stack>
using namespace std;

/* 题目：包含min函数的栈
* 题目描述
* 定义栈的数据结构，请在该类型中实现一个能够得到栈中所含最小元素的min函数（时间复杂度应为O（1））。
*/

/* 题解
*/

class Solution {
public:
	void push(int value) {
		stack_in.push(value);
		if (stack_min.empty()) {
			stack_min.push(value);
		}
		if (stack_min.top() >= value) {
			stack_min.push(value);
		}
	}
	void pop() {		
		if (stack_in.top() == stack_min.top()) {
			stack_min.pop();
		}
		stack_in.pop();
		
	}
	int top() {
		return stack_in.top();
	}
	int min() {
		return stack_min.top();
	}
private:
	stack<int> stack_in;
	stack<int> stack_min;
};

int main() {
	Solution s;
	int num = 10;
	for (int i = 5; i < 10; i++) {
		s.push(num);
		num++;
	}
	cout << s.top() << endl;
	system("pause");
	return 0;
}
```

# 21. 栈的压入、弹出序列

```C++
#include<iostream>
#include<vector>
#include<stack>
using namespace std;

/* 题目：栈的压入、弹出序列
* 题目描述
* 输入两个整数序列，第一个序列表示栈的压入顺序，
请判断第二个序列是否可能为该栈的弹出顺序。
假设压入栈的所有数字均不相等。
例如序列1,2,3,4,5是某栈的压入顺序，
序列4,5,3,2,1是该压栈序列对应的一个弹出序列，
但4,3,5,1,2就不可能是该压栈序列的弹出序列。（注意：这两个序列的长度是相等的）
*/

/* 题解
* 引入一个入栈，判断入栈顶元素是否等于弹出序列第一个元素，不等于，按照入栈序列入栈，等于，弹出，判断下一个
*/

class Solution {
public:
	bool IsPopOrder(vector<int> pushV, vector<int> popV) {
		stack<int> stackIn;
		int id = 0;
		for (int i = 0; i < popV.size(); i++) {
			while (stackIn.empty() || stackIn.top() != popV[i]) {				
				if (id > pushV.size() - 1) {
					return false;
				}
				stackIn.push(pushV[id++]);
			}
			stackIn.pop();
		}
		if (stackIn.empty())
			return true;
		else 
			return false;
	}
};

int main() {
	Solution s;
	vector<int> v1 = { 1,2,3,4,5 };
	vector<int> v2 = { 4,5,3,1,2 };

	cout << s.IsPopOrder(v1, v2)<< endl;

	system("pause");
	return 0;
}
```

# 22. 从上往下打印二叉树

```C++
#include<iostream>
#include<vector>
#include<queue>
using namespace std;

/* 题目：从上往下打印二叉树
* 题目描述
* 从上往下打印出二叉树的每个节点，同层节点从左至右打印。
*/

/* 题解
* 利用队列，首先处理根结点，保存根结点，左孩子结点，右孩子结点，然后弹出根结点，处理左孩子结点，依次入队列
*/

struct TreeNode { 
	int val;
	struct TreeNode *left;
	struct TreeNode *right;
	TreeNode(int x) :val(x), left(NULL), right(NULL) {}
};

class Solution {
public:
	vector<int> PrintFromTopToBottom(TreeNode* root) {
		vector<int> res;
		queue<TreeNode*> q;
		TreeNode *node;
		if (root == NULL) {
			return res;
		}
		q.push(root);		
		while (!q.empty()) {
			node = q.front();
			res.push_back(node->val);
			if (node->left != NULL) {
				q.push(node->left);
			}
			if (node->right != NULL) {
				q.push(node->right);
			}
			q.pop();
		}
		return res;
	}
};

TreeNode* initBTree(int elements[], int size)
{
	if (size < 1)
	{
		return NULL;
	}
	//动态申请size大小的指针数组
	TreeNode **nodes = new TreeNode*[size];
	//将int数据转换为TreeNode节点
	for (int i = 0; i < size; i++)
	{
		if (elements[i] == 0)
		{
			nodes[i] = NULL;
		}
		else
		{
			nodes[i] = new TreeNode(elements[i]);
		}
	}
	queue<TreeNode*> nodeQueue;
	nodeQueue.push(nodes[0]);

	TreeNode *node;
	int index = 1;
	while (index < size)
	{
		node = nodeQueue.front();
		nodeQueue.pop();
		nodeQueue.push(nodes[index++]);
		node->left = nodeQueue.back();
		nodeQueue.push(nodes[index++]);
		node->right = nodeQueue.back();
	}
	return nodes[0];
}

int main() {
	Solution s;
	vector<int> res;
	int nums[] = { 8,6,10,5,7,9,11 };
	TreeNode *tree = initBTree(nums, 7);
	res = s.PrintFromTopToBottom(tree);
	int size = (int)res.size();
	for (int i = 0; i < size; i++) {
		cout << res[i] << "";
	}
	cout << endl;
	system("pause");
	return 0;
}
```

# 23. 二叉搜索树的后序遍历序列

二叉树的遍历分为三种：前序、中序、后序，其中中序遍历最为重要。

A：根结点，B：左结点，C：右结点，前序遍历ABC（根结点，然后同级先左结点后右结点），中序遍历BAC（先左结点后根结点最后右结点），后序遍历顺序BCA（先左结点后右结点最后根结点）

中序遍历的重要性体现在排序上，很多排序都利用到了中序遍历。

后序遍历左子树，后序遍历右子树，访问根结点。

二叉搜索树，左子树的值小于根节点，根节点小于右子树的值。

```C++
#include<iostream>
#include<vector>
#include<queue>
using namespace std;

/* 题目：二叉搜索树的后序遍历序列
* 题目描述
* 输入一个整数数组，判断该数组是不是某二叉搜索树的后序遍历的结果。
* 如果是则输出Yes, 否则输出No。假设输入的数组的任意两个数字都互不相同。
*/

/* 题解
*/

struct TreeNode { 
	int val;
	struct TreeNode *left;
	struct TreeNode *right;
	TreeNode(int x) :val(x), left(NULL), right(NULL) {}
};

class Solution {
public:
	bool VerifySquenceOfBST(vector<int> sequence) {
		int size = sequence.size();
		return bsf(sequence, 0, size - 1);
	}
	bool bsf(vector<int> sequence, int begin, int end) {
		if (sequence.empty() || begin > end) {
			return false;
		}
		int root = sequence.back();
		int loc = begin;
		for (; loc < end; loc++) {
			if (sequence[loc] > root) {
				break;
			}
		}
		for (int i = loc; i < end; i++) {
			if (sequence[i] < root) {
				return false;
			}
		}
		bool left = true, right = true;
		if (loc > begin) {
			left = bsf(sequence, begin, loc - 1);
		}
		if (end > loc) {
			right = bsf(sequence, loc, end - 1);
		}		
		return left && right;
	}
};

TreeNode* initBTree(int elements[], int size)
{
	if (size < 1)
	{
		return NULL;
	}
	//动态申请size大小的指针数组
	TreeNode **nodes = new TreeNode*[size];
	//将int数据转换为TreeNode节点
	for (int i = 0; i < size; i++)
	{
		if (elements[i] == 0)
		{
			nodes[i] = NULL;
		}
		else
		{
			nodes[i] = new TreeNode(elements[i]);
		}
	}
	queue<TreeNode*> nodeQueue;
	nodeQueue.push(nodes[0]);

	TreeNode *node;
	int index = 1;
	while (index < size)
	{
		node = nodeQueue.front();
		nodeQueue.pop();
		nodeQueue.push(nodes[index++]);
		node->left = nodeQueue.back();
		nodeQueue.push(nodes[index++]);
		node->right = nodeQueue.back();
	}
	return nodes[0];
}

int main() {
	Solution s;
	vector<int> sequence = {1,1,3,2,2};
	cout << s.VerifySquenceOfBST(sequence)<<endl;
	system("pause");
	return 0;
}
```

# 24. 二叉树中和为某一值的路径

```C++
#include<iostream>
#include<vector>
#include<queue>
using namespace std;

/* 题目：二叉树中和为某一值的路径
* 题目描述
* 输入一颗二叉树的根节点和一个整数，打印出二叉树中结点值的和为输入整数的所有路径。
* 路径定义为从树的根结点开始往下一直到叶结点所经过的结点形成一条路径。
* (注意: 在返回值的list中，数组长度大的数组靠前)
*/

/* 题解
* 全局变量
*/

struct TreeNode { 
	int val;
	struct TreeNode *left;
	struct TreeNode *right;
	TreeNode(int x) :val(x), left(NULL), right(NULL) {}
};

class Solution {
public:
	vector<vector<int> > FindPath(TreeNode* root, int expectNumber) {
		if (root == NULL) {
			return path;
		}
		list.push_back(root->val);
		expectNumber -= root->val;
		if (expectNumber == 0 && root->left == NULL && root->right == NULL) {
			path.push_back(list);
		}
		FindPath(root->left, expectNumber);
		FindPath(root->right, expectNumber);
		if (!list.empty()) {
			list.pop_back();
		}
		return path;
	}
private:
	vector<vector<int> > path;
	vector<int> list;
};

TreeNode* initBTree(int elements[], int size)
{
	if (size < 1)
	{
		return NULL;
	}
	//动态申请size大小的指针数组
	TreeNode **nodes = new TreeNode*[size];
	//将int数据转换为TreeNode节点
	for (int i = 0; i < size; i++)
	{
		if (elements[i] == 0)
		{
			nodes[i] = NULL;
		}
		else
		{
			nodes[i] = new TreeNode(elements[i]);
		}
	}
	queue<TreeNode*> nodeQueue;
	nodeQueue.push(nodes[0]);

	TreeNode *node;
	int index = 1;
	while (index < size)
	{
		node = nodeQueue.front();
		nodeQueue.pop();
		nodeQueue.push(nodes[index++]);
		node->left = nodeQueue.back();
		nodeQueue.push(nodes[index++]);
		node->right = nodeQueue.back();
	}
	return nodes[0];
}

int main() {
	Solution s;
	int num[] = { 1,3,1,1,1,3,3 };
	TreeNode* tree = initBTree(num, 7);
	vector<vector<int> > path = s.FindPath(tree, 5);
	for (int i = 0; i < (int)path.size(); i++) {
		for (int j = 0; j < (int)path[0].size(); j++) {
			cout << path[i][j] << " ";
		}
		cout << endl;
	}
	cout << endl;
	system("pause");
	return 0;
}
```

# 25. 复制链表的复制

```C++
#include<iostream>
#include<vector>
#include<queue>
using namespace std;

/* 题目：复制链表的复制
* 题目描述
* 输入一个复杂链表（每个节点中有节点值，以及两个指针，一个指向下一个节点，另一个特殊指针指向任意一个节点），
* 返回结果为复制后复杂链表的head。（注意，输出结果中请不要返回参数中的节点引用，否则判题程序会直接返回空）
*/

/* 题解
* 重新创建一个链表的副本，《剑指Offer》
*/

struct RandomListNode {
	int label;
	struct RandomListNode *next, *random;
	RandomListNode(int x) :
		label(x), next(NULL), random(NULL) {
	}
};

class Solution {
public:
	RandomListNode * Clone(RandomListNode* pHead)
	{
		CloneNodes(pHead);
		ConnectRandomNodes(pHead);
		return ReconnectNodes(pHead);
		
	}
	//复制原始链表的任意结点N并创建新节点N'，再把N’链接到N的后面 A-A'-B-B'
	void CloneNodes(RandomListNode* pHead) {
		RandomListNode * pNode = pHead;
		while (pNode != NULL) {
			RandomListNode * pCloned = new RandomListNode(pNode->label);
			pCloned->label = pNode->label;
			pCloned->next = pNode->next;
			pCloned->random = NULL;
			pNode->next = pCloned;

			pNode = pCloned->next;
		}
	}
	//如果原始链表上的结点N的random指向S，则它对应复制结点N'指向S的下一个结点S’,A-A'-B-B'-S-S' A.random = S ,A'.random = S'
	void ConnectRandomNodes(RandomListNode* pHead) {
		RandomListNode * pNode = pHead;
		while (pNode != NULL) {
			RandomListNode * pCloned = pNode->next;
			if (pNode->random != NULL) {
				pCloned->random = pNode->random->next;
			}
			pNode = pCloned->next;
		}
	}
	//将长链表拆分成两个链表，A-B-S，A'-B'-S'
	RandomListNode* ReconnectNodes(RandomListNode* pHead) {
		RandomListNode* pNode = pHead;
		RandomListNode* pClonedHead = NULL;
		RandomListNode* pClonedNode = NULL;
		if (pNode != NULL) {
			pClonedHead = pClonedNode = pNode->next;
			pNode->next = pClonedNode->next;
			pNode = pNode->next;
		}
		while (pNode != NULL) {
			pClonedNode->next = pNode->next;//链表链起来
			pClonedNode = pClonedNode->next;
			pNode->next = pClonedNode->next;
			pNode = pNode->next;
		}
		return pClonedHead;
	}
};

int main() {
	Solution s;
	RandomListNode * head = NULL;
	s.Clone(head);
	system("pause");
	return 0;
}
```

# 26. 二叉搜索树与双向链表

输入一棵二叉搜索树，将该二叉搜索树转换成一个排序的双向链表。要求不能创建任何新的结点，只能调整树中结点指针的指向。

题解：中序遍历二叉树的结点，根节点与其左子树最大的一个结点链接起来，同时与其右子树中最小的一个结点链接起来。按照中序遍历的顺序，当遍历转换到根节点时，此时左子树已经转换为一个排序的链表了，并且处在链表中的最后一个结点就是当前值最大的结点，将这个值与根结点链接起来，接着去转换右子树。

遍历和转换过程是一样的，所以采用递归的方法。
```C++
#include<iostream>
using namespace std;

struct  TreeNode {
	int val;
	struct TreeNode *left;
	struct TreeNode *right;
	TreeNode(int x): val(x), left(NULL), right(NULL) {
	}
};

class Solution {
public:
	TreeNode * Convert(TreeNode* pRootOfTree) {
		TreeNode *pLastNodeOfList = NULL;
		ConvertNode(pRootOfTree, &pLastNodeOfList);
		TreeNode *pHeadOfList = pLastNodeOfList;//返回头节点
		while (pHeadOfList != NULL && pHeadOfList->left != NULL) {
			pHeadOfList = pHeadOfList->left;
		}
		return pHeadOfList;
	}
	void ConvertNode(TreeNode* pNode, TreeNode** pLastNodeInList) {
		if (pNode == NULL)
			return;
		TreeNode *pCurrent = pNode;
		if (pCurrent->left != NULL)
			ConvertNode(pCurrent->left, pLastNodeInList);
		pCurrent->left = *pLastNodeInList;
		if (*pLastNodeInList != NULL) {//空指针不能指向别的
			(*pLastNodeInList)->right = pCurrent;
		}
		*pLastNodeInList = pCurrent;
		if (pCurrent->right != NULL)
			ConvertNode(pCurrent->right, pLastNodeInList);
	}
};

int main() {
	Solution s;
	TreeNode * head = NULL;
	s.Convert(head);
	system("pause");
	return 0;
}
```

# 27. 字符串的排列

输入一个字符串,按字典序打印出该字符串中字符的所有排列。例如输入字符串abc,则打印出由字符a,b,c所能排列出来的所有字符串abc,acb,bac,bca,cab和cba。

```C++
#include<iostream>
#include<string>
#include<algorithm>
#include<vector>
#include<iterator>
using namespace std;

class Solution {
public:
	vector<string> Permutation(string str) {
		vector<string> res;
		if (str.empty())
			return res;
		int size = (int)str.size();
		Permutation(str, 0, size, res);
		sort(res.begin(),res.end());//有重复的
		vector<string>::iterator ite = unique(res.begin(), res.end());
		/*unique的功能是去除相邻的重复元素（只保留一个），还有一个容易忽视的特性是它并不真正把重复的元素删除，
		unique只是把重复的元素放到容器的后面，而它本身会返回一个迭代器，指向这些元素的开始部分。*/
		res.erase(ite, res.end());
		/*for (vector<string>::iterator it = res.begin(); (it + 1) != res.end();) {
			if (*it == *(it + 1)) {
				//res.erase(it+1);
				it = res.erase(it);//vector erase之后产生野指针
			}
			else {
				it++;
			}
		}*/
		return res;
	}

	//传递引用给函数与传递指针的效果是一样的,被调函数的形参就成为原来主调函数中的实参变量或对象的一个别名来使用，
	//所以在被调函数中对形参变量的操作就是对其相应的目标对象（在主调函数中）的操作
	void Permutation(string str, int begin, int end, vector<string> &res) {
		if (begin == end){
			res.push_back(str);
		}
		for (int i = begin; i < end; i++) {
			char tmp = str[i];
			str[i] = str[begin];
			str[begin] = tmp;
			Permutation(str, begin + 1, end, res);
			//再换回来
			tmp = str[i];
			str[i] = str[begin];
			str[begin] = tmp;
		}		
	}
};

int main() {
	Solution s;
	string str = "aba";
	vector<string> res;
	res = s.Permutation(str);
	/*for (vector<string>::iterator it = res.begin(); it < res.end(); it++) {
		cout << *it << endl;
	}*/
	for (auto i : res)
		cout << i << " ";
	cout << endl;
	system("pause");
	return 0;
}
```

# 28. 数组中出现次数超过一半的数字

数组中有一个数字出现的次数超过数组长度的一半，请找出这个数字。例如输入一个长度为9的数组{1,2,3,2,2,2,5,4,2}。由于数字2在数组中出现了5次，超过数组长度的一半，因此输出2。如果不存在则输出0。

```C++
#include<iostream>
#include<vector>
using namespace std;

class Solution {
public:
	int MoreThanHalfNum_Solution(vector<int> numbers) {
		int size = numbers.size();
		if (size == 0)
			return 0;

		int result = numbers[0];
		int times = 1;
		for (int i = 1; i < size; i++) {
			if (times == 0) {
				result = numbers[i];
				times = 1;
			}
			else if (result == numbers[i]) {
				times++;
			}
			else
				times--;
		}

		//检查输入合法性
		times = 0;
		for (int i = 0; i < size; i++) {
			if (result == numbers[i])
				times++;
		}
		if (times *2 <= size)//建议不要用size/2
			return 0;
		return result;
	}
	
};

int main() {
	Solution s;
	int res;
	vector<int> num = {1,2,3,2,2,2,5,4,2};
	res = s.MoreThanHalfNum_Solution(num);
	cout << res << endl;
	system("pause");
	return 0;
}
```

# 附. 快速排序算法的实现

快速排序算法：首先在数组中选择一个数字，这个数字一般是数组的第一个数，然后将比这个数小的数字移到该数的左边，比这个数大的数字移到该数的右边。

最坏情况复杂度n^2，平均时间复杂度nlogn，原址排序

快速排序将数组划分为四个部分，第一个部分都是比该数小的数，第二个部分都是比该数大的数，第三个部分是待处理部分，第四部分是该数。

C++代码实现：
```C++
#include<iostream>
#include<vector>
using namespace std;

void swap(int &a, int &b) {
	int tmp = a;
	a = b;
	b = tmp;
}

int Partition(vector<int> &numbers, int start, int end) {
	int i = start - 1;
	int x = numbers[end];
	for (int j = start; j < end; j++) {
		if (numbers[j] <= x) {
			i++;
			swap(numbers[i], numbers[j]);
		}
	}
	swap(numbers[end], numbers[i + 1]);
	return i + 1;
}

void QuickSort(vector<int> &numbers, int start, int end) {
	if (start < end) {
		int index = Partition(numbers, start, end);
		Partition(numbers, start, index - 1);
		Partition(numbers, index + 1, end);
	}
}

int main() {
	vector<int> num = { 1,2,3,2,2,2,5,4,2 };
	QuickSort(num, 0, num.size() - 1);
	for (auto i : num)
		cout << i << "";
	cout << endl;
	/*int a = 1, b = 2;
	swap(a, b);
	cout << a << " " << b << endl;*/
	system("pause");
	return 0;
}
```

# 29. 最小的K个数

输入n个整数，找出其中最小的K个数。例如输入4,5,1,6,2,7,3,8这8个数字，则最小的4个数字是1,2,3,4,。

自己的方法：快排取出前k个数。

其他的方法：巧用Partition函数（不必完全排序，查找n个数中第k大的数字，index == k - 1 ?），或者用二叉树数据结构调整（堆，红黑树）。

大小为k数据的二叉树，需要做3件事：第一，在k个整数中找到最大数；第二，有可能在容器中删除这个最大数；第三，有可能插入一个新的数字。上述3个操作在O(logk)的时间内完成，对于n输入的数组而言，总的时间复杂度为O(nlogk)。

最大堆：O(1)时间找到最大值，O(logk)完成插入和删除操作，其根结点的大小总是大于其子结点的大小。（实现最大堆需要一定的代码量）

红黑树：把结点分为红、黑两种颜色并根据一定的规则确保树在一定程度上是平衡的，其查找、删除和插入操作时间复杂度都是O(logk)。

STL中的set和multiset是基于红黑树实现的。

```C++
#include<iostream>
#include<vector>
using namespace std;

class Solution {
public:
	vector<int> GetLeastNumbers_Solution(vector<int> input, int k) {
		vector<int> res;
		int size = input.size();
		if (size == 0 || k > size) 
			return res;
		QuickSort(input, 0, size - 1);		
		for (int i = 0; i < k; i++) {
			res.push_back(input[i]);
		}
		return res;
	}

	void QuickSort(vector<int> &num, int begin, int end) {
		if (begin < end) {
			int index = Partition(num, begin, end);
			if(index > begin)//判断条件必加
				QuickSort(num, begin, index - 1);//递归QuickSort，非Partition
			if (index < end)
				QuickSort(num, index + 1, end);
		}
	}

	int Partition(vector<int> &num, int begin, int end) {
		int i = begin - 1;
		int x = num[end];
		for (int j = begin; j < end; j++) {
			if (num[j] <= x) {
				i++;
				swap(num[j], num[i]);
			}
		}
		swap(num[end], num[i + 1]);
		return i + 1;
	}

	void swap(int &a, int &b) {
		int tmp = a;
		a = b;
		b = tmp;
	}
};

int main() {
	Solution s;
	vector<int> num = { 4,5,1,6,2,7,3,8 };
	vector<int> res;
 	res = s.GetLeastNumbers_Solution(num, 4);
	for (auto i : res) {
		cout << i << " ";
	}
	system("pause");
	return 0;
}

```

基于Partition函数的实现：
```C++
#include<iostream>
#include<vector>
using namespace std;

class Solution {
public:
	vector<int> GetLeastNumbers_Solution(vector<int> input, int k) {
		vector<int> res;
		int size = input.size();
		if (size == 0 || k > size) 
			return res;
		int index = Partition(input, 0, size - 1);
		while (index != k - 1) {
			if (index > k - 1) {
				index = Partition(input, 0, index - 1);
			}
			else {
				index = Partition(input, index + 1, size - 1);
			}
		}
		for (int i = 0; i < k; i++) {
			res.push_back(input[i]);
		}
		return res;
	}

	int Partition(vector<int> &num, int begin, int end) {
		int i = begin - 1;
		int x = num[end];
		for (int j = begin; j < end; j++) {
			if (num[j] <= x) {
				i++;
				swap(num[j], num[i]);
			}
		}
		swap(num[end], num[i + 1]);
		return i + 1;
	}
};

int main() {
	Solution s;
	vector<int> num = { 4,5,1,6,2,7,3,8 };
	vector<int> res;
 	res = s.GetLeastNumbers_Solution(num, 4);
	for (auto i : res) {
		cout << i << " ";
	}
	system("pause");
	return 0;
}
```

基于红黑树的实现：
```C++

```

# 附. 迭代器

```C++
for(auto it = s.begin(); it != s.end() && !isspace(*it); ++it)
	*it = toupper(*it);
```
泛型编程，C++程序员习惯性在范围for语句中使用 `!=` 和 `==`，因为所有的标准库提供的容器上都提供了这种操作，相对于使用下标操作，使用迭代器的方式更加广泛。

所以，养成良好的编程风格是至关重要的。

比如在使用下标的过程中，首先要判断对象是否为空。

# 附. 二分查找下标问题
在二分搜索程序中，用的是`mid = beg + (end - beg)/2`，而非`mid = (beg + end)/2`，第一种原因是避免溢出。其他原因，参考其他人的回答如下：

很简单。这个如果是数组下标还行的通，但如果是指针，那`beg + end`这个操作本身就有炸范围的风险。

另外从概念上，`end - beg`这个操作，得到的是有序序列中两个元素的距离增量。所以最后的逻辑能够分解为：求距离增量，然后折半，最后加回基址上边去。

而`beg + end`这个操作本身得到的值，并没有明确的意义。所以虽然在数学上两个式子并没有区别，但如果追究求表达式的分步运算，则后一个式子存在意义不明确的运算操作，可读性和概念性上都差一点。

综上所述：

第一 前者不会产生溢出，而后者可能会。

第二 前者适用于对迭代器和指针的操作，而后者不行。

# 30. 连续子数组的最大和

HZ偶尔会拿些专业问题来忽悠那些非计算机专业的同学。今天测试组开完会后,他又发话了:在古老的一维模式识别中,常常需要计算连续子向量的最大和,当向量全为正数的时候,问题很好解决。但是,如果向量中包含负数,是否应该包含某个负数,并期望旁边的正数会弥补它呢？例如:{6,-3,-2,7,-15,1,2,2},连续子向量的最大和为8(从第0个开始,到第3个为止)。给一个数组，返回它的最大连续子序列的和，你会不会被他忽悠住？(子向量的长度至少是1)

采用动态规划的思路，i连续子数组的最大和等于i-1连续子数组的最大和加上第i个数，如果i-1连续子数组的和小于等于0，i连续子数组的最大和等于第i个数；否则，等于i-1连续子数组最大和加上第i个数。

目标：`max(f(i))`，当 `f(i-1) > 0` 时，`f(i) = f(i-1) + array[i]`；当 `f(i-1) <= 0` 时，`f(i) = array[i]`。

记录每个`f(i)`的值：`res`，求最大的`f(i)`：`greatest_sum`

```C++
#include<iostream>
#include<vector>
using namespace std;

class Solution {
public:
	int FindGreatestSumOfSubArray(vector<int> array) {
		int size = (int)array.size();
		if (size == 0)
			return 0;
		int res = 0;
		int greatest_sum = array[0];
		for (int i = 0; i < size; i++) {
			if (res <= 0) 
				res = array[i];
			else 
				res += array[i];

			if (res > greatest_sum)
				greatest_sum = res;
		}
		return greatest_sum;
	}
};

int main() {
	Solution s;
	vector<int> num = { 6,-3,-2,7,-15,1,2,2 };
	int res = s.FindGreatestSumOfSubArray(num);
	cout << res << endl;
	system("pause");
	return 0;
}
```

# 31. 整数中1出现的次数

（从1到n整数中1出现的次数）

求出1-13的整数中1出现的次数,并算出100~1300的整数中1出现的次数？为此他特别数了一下1-13中包含1的数字有1、10、11、12、13因此共出现6次,但是对于后面问题他就没辙了。ACMer希望你们帮帮他,并把问题更加普遍化,可以很快的求出任意非负整数区间中1出现的次数（从1 到 n 中1出现的次数）。

此题是整数中1出现的次数，不是带1的整数出现了多少次。

找出规律：

参考大神的解答：归纳总结

在个位数上，1会每隔10出现一次，1，11，21，31...，以10为一个阶梯，每一个完整的阶梯里面都有一个1。在不完整的阶梯里需要判断这个阶梯中会不会出现1，如果最后露出来的部分是小于1的话，则不可能出现1。

于是各位上1出现的次数：`n/10 * 1  + (n % 10 != 0 ? 1 : 0)`

十位数出现1的情况是10-19，其中包含了个位数部分出现1的情况，10-19每隔100出现一次，阶梯是100，数字317的阶梯为：0-99，100-199，200-299三段完整的阶梯，每隔阶梯里面会出现10次1（10-19），最后分析那段不完整的阶梯300-317，如果露出来的数大于19，则有10个1，如果小于10，肯定不会出现十位数的1，如果K在10-19之间，计算结果应该是K-10+1。

于是十位数上1出现的次数：
* 设`k = n % 100`，即为不完整阶梯段的数字
* 归纳式：`(n/100) *10 + ( if(k > 19) 10 else if(k < 10) 0 else k - 10 + 1)`

百位1：同上归纳如下
* 设k = n % 1000
* 归纳式为：`(n / 1000) * 100 + (if(k >199) 100 else if(k < 100) 0 else k - 100 + 1)`

将1加入归纳式：
* k = n % 10
* 个位数上1的个数为：`n / 10 * 1 + (if(k > 1) 1 else if(k < 1) 0 else k - 1 + 1)`

更抽象的归纳：
设i为计算1所在的位数，i=1表示计算个位数的1的个数，10表示计算十位数的1的个数等等
* `k = n % (i * 10)`
* `count(i) = (n / (i * 10)) * i + (if(k > i * 2 - 1) i else if(k < i) 0 else k - i + 1)`

```C++
sum = sum(count(i)),
i = Math.pow(10,j),
0 <= j <= log10(n)
```
实现代码：
```C++
#include<iostream>
using namespace std;

class Solution {
public:
	int NumberOf1Between1AndN_Solution(int n)
	{
		int count = 0;//整数中1出现的次数
		if (n <= 0)
			return 0;
		int k;
		for (int i = 1; i <= n; i *= 10) {
			k = n % (i * 10);
			count += n / (i * 10) * i;
			if (k > 2 * i - 1) {
				count += i;
			}
			if (k >= i && k <= 2 * i - 1) {
				count += k - i + 1;
			}
		}
		return count;
	}
};

int main() {
	Solution s;
	int num = 10;
	int res = s.NumberOf1Between1AndN_Solution(num);
	cout << res << endl;
	system("pause");
	return 0;
}
```

# 32. 把数组排成最小的数

输入一个正整数数组，把数组里所有数字拼接起来排成一个数，打印能拼接出的所有数字中最小的一个。例如输入数组{3，32，321}，则打印出这三个数字能排成的最小数字为321323。

将数字拼接起来有可能出现大数问题，即用int表示有可能会溢出，所以首先将整型数组转换成string数组，然后将string数组进行排序，最后将排好序的字符串数组拼接出来。

这个问题的关键就是如何指定排序规则对字符串数组进行排序。

假设有两个字符串a和b，指定排序规则如下：
* 若 `ab > ba` ，则 `a > b` ;
* 若 `ab < ba` ，则 `a < b` ;
* 若 `ab = ba` ，则 `a = b` ;

解释说明：
比如 "2" < "21" ，但是因为 "212" < "221"，所以排序后为 "21" < "2"。

[sort函数解析](https://blog.csdn.net/arcobaleno1996/article/details/81510306)

sort函数在不加第三个参数的时候是升序排列。
```C++
bool compare(int a, int b){
	return a < b;//升序排列，如果改为 a > b,降序排列。
}
```
排序的数据类型不局限于整数，只要是定义了小于运算的类型都可以，比如字符串类string。
如果是没有定义小于运算的数据类型，或者想改变排序的顺序，就要用到第三参数——比较(compare)函数。比较函数是一个自己定义的函数，返回值是bool型，它规定了什么样的关系才是“小于”。
比较时sort函数根据comp函数进行判断输的大小，系统默认 `a > b` 时返回为真，那么最终得到的排序结果也相应的从小到大变成从大到小。

`static函数`

static函数与普通函数的区别：

用static修饰的函数，本限定在本源码文件中，不能被本源码文件以外的代码文件调用。而普通的函数，默认是extern的，也就是说，可以被其它代码文件调用该函数。

在函数的返回类型前加上关键字static，函数就被定义成为静态函数。普通 函数的定义和声明默认情况下是extern的，但静态函数只是在声明他的文件当中可见，不能被其他文件所用。因此定义静态函数有以下好处：

1. 其他文件中可以定义相同名字的函数，不会发生冲突。

2. 静态函数不能被其他文件所用。

提交代码：
```C++
#include<iostream>
#include<vector>
#include<string>
#include<algorithm>
using namespace std;

class Solution {
public:
	string PrintMinNumber(vector<int> numbers) {
		int length = numbers.size();
		if (length == 0)
			return "";
		sort(numbers.begin(), numbers.end(), cmp);
		string res;
		for (int i = 0; i < numbers.size(); i++) {
			res += to_string(numbers[i]);
		}
		return res;
	}

	//新定义的排序关系，当 A < B 时，即 ab < ba 时，a < b
	static bool cmp(int a, int b) {
		string A = to_string(a) + to_string(b);
		string B = to_string(b) + to_string(a);
		return A < B;
	}
};

int main() {
	Solution s;
	vector<int> num = { 3,32,321 };
	string res = s.PrintMinNumber(num);
	cout << res << endl;
	system("pause");
	return 0;
}

```
# 33. 丑数

把只包含质因子2、3和5的数称作丑数（Ugly Number）。例如6、8都是丑数，但14不是，因为它包含质因子7。 习惯上我们把1当做是第一个丑数。求按从小到大的顺序的第N个丑数。

解题思路：
对数一个一个判断的话时间复杂度较大，如果是直接生成丑数的话就可以直接找到所需要的丑数，第一个丑数是1，其余的丑数是前面的丑数的2，3，5倍，所以生成丑数的方法是，由前面的丑数*2，*3，*5选取生成丑数的最小值放在数组的尾部，但是对数组所有的数*2，*3，*5生成的丑数一部分小于数组目前最大的丑数，一部分大于数组目前最大的丑数，我们不需要比其小的丑数，于是记录一个下标，t2，也就是下标t2之前生成的数都小于当前最大丑数，同时设置t3，t5。

```C++
#include<iostream>
#include<vector>
#include<algorithm>
using namespace std;

class Solution {
public:
	int GetUglyNumber_Solution(int index) {
		if (index < 7) return index;
		vector<int> uglyNumbers(index);
		uglyNumbers[0] = 1;
		int t2 = 0, t3 = 0, t5 = 0;
		for (int i = 1; i < index; i++) {
			uglyNumbers[i] = min(uglyNumbers[t2] * 2, min(uglyNumbers[t3] * 3, uglyNumbers[t5] * 5));
			if (uglyNumbers[i] == uglyNumbers[t2] * 2) t2++;
			if (uglyNumbers[i] == uglyNumbers[t3] * 3) t3++;
			if (uglyNumbers[i] == uglyNumbers[t5] * 5) t5++;
		}
		return uglyNumbers[index - 1];
	}
};

int main() {
	Solution s;
	int num = 255;
	int res = s.GetUglyNumber_Solution(num);
	cout << res << endl;
	system("pause");
	return 0;
}
```

# 34. 第一个只出现一次的字符
在一个字符串(0<=字符串长度<=10000，全部由字母组成)中找到第一个只出现一次的字符,并返回它的位置, 如果没有则返回 -1（需要区分大小写）.

第一种垃圾思路：当访问到某个字符时，拿这个字符与后面的字符相比较，如果在后面没有发现重复的字符，则该字符就是只出现一次的字符，时间复杂度O(n^2)。

第二种思路，统计每个字符出现的次数，需要一个数据容器来存放每个字符的次数。在这个数据容器中可以根据字符来查找它出现的次数，也就是说这个容器的作用是把一个字符映射成一个数字。

在常用的数据容器中，哈希表正是这个用途。

定义哈希表的键值Key是字符，而值Value是该字符出现的次数。同时需要从头扫描字符串两次，第一次每扫描到一个字符就将哈希表中对应的次数加1，第二次，扫描就能从哈希表中得到该字符出现的次数，找到第一个只出现一次的字符。

哈希表是一种复杂的数据结构，而且C++标准模板库中并没有实现哈希表。需要创建一个哈希表。

这个简单的哈希表，可以用一个256个元素的数组来表示，因为ASCII码字符的个数是256个，数组的下标对应着哈希表的键值，数组的值对应着哈希表的值。

```C++
#include<iostream>
#include<vector>
#include<string>
#include<algorithm>
using namespace std;

class Solution {
public:
	int FirstNotRepeatingChar(string str) {
		int len = str.size();
		if (len == 0)
			return -1;
		int hashTable[256] = {0};
		int res = -1;
		for (int i = 0; i < len; i++) {
			hashTable[str[i] - '0']++;
		}
		for (int i = 0; i < len; i++) {
			if (hashTable[str[i] - '0'] == 1) {
				res = i;
				break;
			}
		}
		return res;
	}
};

int main() {
	Solution s;
	string str = "22233";
	int res = s.FirstNotRepeatingChar(str);
	cout << res << endl;
	system("pause");
	return 0;
}
```

# 35. 数组中的逆序对

在数组中的两个数字，如果前面一个数字大于后面的数字，则这两个数字组成一个逆序对。输入一个数组,求出这个数组中的逆序对的总数P。并将P对1000000007取模的结果输出。 即输出P%1000000007

题目保证输入的数组中没有的相同的数字

数据范围：

	对于%50的数据,size<=10^4

	对于%75的数据,size<=10^5

	对于%100的数据,size<=2*10^5

示例1

输入  1,2,3,4,5,6,7,0
输出  7

代码加速问题：

在此题的top回答中，有很多在前面写了这么一段代码
```C++
static const auto io_sync_off = []() {
    ios_base::sync_with_stdio(false);
    cin.tie(nullptr);
    cout.tie(nullptr);
    return nullptr;
}( );
```
这段代码相当于
```C++
static const auto function(){

}

static const auto io_sync_off = function();
```
C++11 的新特性，lambda匿名函数。[参考](https://blog.csdn.net/qq_32320399/article/details/81518476)

这里的const是修饰函数的返回值。

std::cin 和 std::cout，兼容了C语言的输入输出，其目的是为了解除这种关系。

[STL的copy函数](https://www.cnblogs.com/heyonggang/p/3265142.html)

```C++
template<class InputIterator, class OutputIterator>
OutputIterator copy(  
	InputIterator _First,   
	InputIterator _Last,   
	OutputIterator _DestBeg  
);  
```

主要问题，递归函数的调用顺序：

一层一层的返回

[参考](https://blog.csdn.net/caoshangpa/article/details/80362743)

递归的调用每层每层的，最里面一层一直执行到函数结束再返回执行上一层。

```C++
#include<iostream>
#include<vector>
#include<algorithm>
using namespace std;

static const auto io_sync_off = []() {
	ios_base::sync_with_stdio(false);
	cin.tie(nullptr);
	cout.tie(nullptr);
	return nullptr;
}();

class Solution {
public:
	static constexpr int P = 1000000007;

	int InversePairs(vector<int> data) {
		if (data.empty())return 0;
		vector<int> copy(data);
		return merge_sort(data, copy, 0, data.size() - 1);
	}

	int merge_sort(vector<int> &data, vector<int> &copy, int begin, int end) {
		if (begin == end) {//终止递归调用语句
			copy[begin] = data[begin];
			return 0;
		}
		int mid = begin + (end - begin) / 2;
		int left = merge_sort(copy, data, begin, mid);//这个的data和copy不能交换
		int right = merge_sort(copy, data, mid + 1, end);
		int i = mid;
		int j = end;
		int indexcopy = end;
		int cnt = 0;
		while (i >= begin && j >= mid + 1) {
			if (data[i] > data[j]) {
				copy[indexcopy--] = data[i--];
				(cnt += j - mid) %= P;
			}
			else {
				copy[indexcopy--] = data[j--];
			}

		}
		for (; i >= begin; i--) 
			copy[indexcopy--] = data[i];
		for (; j >= mid + 1; j--) 
			copy[indexcopy--] = data[j];

		return (left + right + cnt) % P;
	}
};

int main() {
	Solution s;
	vector<int> num = {7,5,6,4};
	int res = s.InversePairs(num);
	cout << res << endl;
	system("pause");
	return 0;
}
```

# 36. 两个链表中的第一个公共结点

两个链表一旦有公共结点，说明它们的尾部一定相同，那么让长的链表移动到和短的链表相同的长度进行比较。

```C++
#include<iostream>
#include<vector>
#include<algorithm>
#include<stack>
using namespace std;

struct ListNode {
	int val;
	struct ListNode *next;
	ListNode(int x) :
		val(x), next(NULL) {
	}
};

class Solution {
public:
	ListNode * FindFirstCommonNode(ListNode* pHead1, ListNode* pHead2) {
		if (pHead1 == NULL || pHead2 == NULL) return NULL;

		int length1 = GetLength(pHead1);
		int length2 = GetLength(pHead2);

		int lengthDif = length1 - length2;
		ListNode * longList = pHead1;
		ListNode * shortList = pHead2;

		if (length2 > length1) {
			ListNode * longList = pHead2;
			ListNode * shortList = pHead1;
			lengthDif = length2 - length1;
		}

		while (lengthDif > 0) {
			longList = longList->next;
			lengthDif--;
		}

		while ((longList != NULL) && (longList->val != shortList->val)) {
			longList = longList->next;
			shortList = shortList->next;
		}
				
		return longList;
	}

	int GetLength(ListNode * phead) {
		int length = 0;
		ListNode * pNode = phead;
		while (pNode != NULL) {
			length++;
			pNode = pNode->next;
		}
		return length;
	}
};

//尾插法建立单链表
ListNode * Creat_LinkList_R()
{
	int x;
	ListNode *head, *p, *tail;                    //tail是尾指针
	head = (ListNode*)malloc(sizeof(ListNode));
	if (head == NULL)
		return head;
	head->next = NULL;
	tail = head;                                  //一开始尾指针指向头指针的位置
	cout << "请输入要录入的数以0结束" << endl;
	cin >> x;
	head->val = x;
	while ((cin >> x) && (x != 0))
	{
		p = (ListNode*)malloc(sizeof(ListNode));
		if (p == NULL)
			return head;
		p->val = x;
		tail->next = p;                          //将p插入到尾节点的后面
		tail = p;                                //修改尾节点的指向
		tail->next = NULL;                       //将尾节点的指针域修改为空
	}
	return head;
}

int main() {
	Solution s;
	ListNode *list1, *list2;
	list1 = Creat_LinkList_R();
	list2 = Creat_LinkList_R();

	ListNode * res = s.FindFirstCommonNode(list1, list2);
	cout << res->val << endl;
	system("pause");
	return 0;
}
```

# 37. 数字在排序数组中出现的次数

在查找算法中，二分查找的优势。

统计一个数字在排序数组中出现的次数。

顺序查找：
```C++
#include<iostream>
#include<vector>
using namespace std;

class Solution {
public:
	int GetNumberOfK(vector<int> data, int k) {
		if (data.empty())
			return 0;
		int cnt = 0;
		for (int i = 0; i < data.size(); i++) {
			if (data[i] == k)
				cnt++;
		}
		return cnt;
	}
};

int main() {
	Solution s;
	vector<int> num = { 1,2,3,3,3,3,4,5 };
	cout << s.GetNumberOfK(num, 3) << endl;
	system("pause");
	return 0;
}
```

更好的方法：二分查找算法，主要目的确定第一个数字k出现的位置以及最后一个数字k出现的次数。

用二分查找法直接找到数字k的位置，在二分查找中，总是将中间的数字与k进行比较，如果中间的数字大于k，那么数字k在前半段；如果中间数字小于k，那么数字k在后半段；如果中间数字等于k，先判断这个k是否是第一个k，如果中间数字的前一个数字不是k，那么这个k就是第一个k，如果前一个数字是k，则第一个k位于前半段。

```C++
#include<iostream>
#include<vector>
using namespace std;

class Solution {
public:
	int GetNumberOfK(vector<int> data, int k) {
		if (data.empty())
			return 0;
		int cnt = 0;
		int firstKindex = GetFirstK(data, 0, data.size() - 1, k);
		int lastKindex = GetLastK(data, 0, data.size() - 1, k);
		if (firstKindex > -1 && lastKindex > -1) {
			cnt = lastKindex - firstKindex + 1;
		}
		return cnt;
	}

	int GetFirstK(vector<int> data, int begin, int end, int k) {
		if (begin > end) return -1;//递归结束语句
		int mid = begin + (end - begin) / 2;
		if (data[mid] == k) {
			if ((mid > 0 && data[mid - 1] != k) || mid == 0)
				return mid;
			else
				end = mid - 1;
		}
		else if (data[mid] > k) {
			end = mid - 1;
		}
		else {
			begin = mid + 1;
		}
		return GetFirstK(data, begin, end, k);
	}

	int GetLastK(vector<int> data, int begin, int end, int k) {
		if (begin > end) return -1;//递归结束语句
		int mid = begin + (end - begin) / 2;
		if (data[mid] == k) {
			if ((mid < end && data[mid + 1] != k) || mid == end)
				return mid;
			else
				begin = mid + 1;
		}
		else if (data[mid] > k) {
			end = mid - 1;
		}
		else {
			begin = mid + 1;
		}
		return GetLastK(data, begin, end, k);
	}
};

int main() {
	Solution s;
	vector<int> num = { 1,2,3,3,3,3,4,4,5 };
	cout << s.GetNumberOfK(num, 4) << endl;
	system("pause");
	return 0;
}

```

运行时间和占用内存数比上个多了，但是理论分析时间复杂度从O(n)降低到O(logn)

# 38. 二叉树的深度

输入一棵二叉树，求该树的深度。从根结点到叶结点依次经过的结点（含根、叶结点）形成树的一条路径，最长路径的长度为树的深度。

递归：如果一个树只有一个结点，那么它的深度为1，如果根结点只有左子树没有右子树，树的深度是左子树的深度加1；如果既有左子树又有右子树，树的深度是左右子树的最大的深度加1。

```C++
#include<iostream>
#include<vector>
#include<queue>
#include<algorithm>
using namespace std;

struct TreeNode {
	int val;
	struct TreeNode *left;
	struct TreeNode *right;
	TreeNode(int x) :
		val(x), left(NULL), right(NULL) {
	}
};

class Solution {
public:
	int TreeDepth(TreeNode* pRoot)
	{
		if (pRoot == NULL) 
			return 0;

		return max(TreeDepth(pRoot->left), TreeDepth(pRoot->right)) + 1;
	}
};

TreeNode* initBTree(int elements[], int size)
{
	if (size < 1)
	{
		return NULL;
	}
	//动态申请size大小的指针数组
	TreeNode **nodes = new TreeNode*[size];
	//将int数据转换为TreeNode节点
	for (int i = 0; i < size; i++)
	{
		if (elements[i] == 0)
		{
			nodes[i] = NULL;
		}
		else
		{
			nodes[i] = new TreeNode(elements[i]);
		}
	}
	queue<TreeNode*> nodeQueue;
	nodeQueue.push(nodes[0]);

	TreeNode *node;
	int index = 1;
	while (index < size)
	{
		node = nodeQueue.front();
		nodeQueue.pop();
		nodeQueue.push(nodes[index++]);
		node->left = nodeQueue.back();
		nodeQueue.push(nodes[index++]);
		node->right = nodeQueue.back();
	}
	return nodes[0];
}

int main() {
	Solution s;
	int nums[] = { 1,2,3,4,5,0,6,0,0,7,0};
	TreeNode *tree1 = initBTree(nums, 11);
	cout << s.TreeDepth(tree1)<< endl;
	system("pause");
	return 0;
}
```

# 39. 平衡二叉树

输入一棵二叉树，判断该二叉树是否是平衡二叉树。

每个结点的左右子树的深度都不超过1，那么按照定义它就是平衡二叉树。

```C++
#include<iostream>
#include<vector>
#include<queue>
#include<algorithm>
using namespace std;

struct TreeNode {
	int val;
	struct TreeNode *left;
	struct TreeNode *right;
	TreeNode(int x) :
		val(x), left(NULL), right(NULL) {
	}
};

class Solution {
public:
	bool IsBalanced_Solution(TreeNode* pRoot) {
		if (pRoot == NULL) return true;
		int left = TreeDepth(pRoot->left);
		int right = TreeDepth(pRoot->right);
		if (abs(left - right) > 1)
			return false;
		return IsBalanced_Solution(pRoot->left) && IsBalanced_Solution(pRoot->right);
	}

	int TreeDepth(TreeNode* pRoot) {
		if (pRoot == NULL)
			return 0;
		return max(TreeDepth(pRoot->left), TreeDepth(pRoot->right)) + 1;
	}
};

TreeNode* initBTree(int elements[], int size)
{
	if (size < 1)
	{
		return NULL;
	}
	//动态申请size大小的指针数组
	TreeNode **nodes = new TreeNode*[size];
	//将int数据转换为TreeNode节点
	for (int i = 0; i < size; i++)
	{
		if (elements[i] == 0)
		{
			nodes[i] = NULL;
		}
		else
		{
			nodes[i] = new TreeNode(elements[i]);
		}
	}
	queue<TreeNode*> nodeQueue;
	nodeQueue.push(nodes[0]);

	TreeNode *node;
	int index = 1;
	while (index < size)
	{
		while(nodeQueue.front() == NULL)
			nodeQueue.pop();
		node = nodeQueue.front();
		nodeQueue.pop();
		nodeQueue.push(nodes[index++]);
		node->left = nodeQueue.back();
		nodeQueue.push(nodes[index++]);
		node->right = nodeQueue.back();
	}
	return nodes[0];
}

int main() {
	Solution s;
	int nums[] = { 1,2,3,0,0,0,6,8,0};
	TreeNode *tree1 = initBTree(nums, 9);
	cout << s.IsBalanced_Solution(tree1)<< endl;
	system("pause");
	return 0;
}
```

# 40. 数组中只出现一次的数字

一个整型数组里除了两个数字之外，其他的数字都出现了偶数次。请写程序找出这两个只出现一次的数字。

如果数组中只有一个数字出现一次，其余的数字都出现了偶数次，那么可以采用将数组中的每个元素都异或一边，得到的结果就是数组中只出现一次的数字。

但是在数组中有两个出现一次的数字，这两个数字的异或结果一定不为零。我们可以把原始数组分为两个子数组，使得每个子数组只包含一个出现一次的数字。

首先还是将所有数组中的数字都异或一遍，得到异或的结果，这个结果不为0，将结果中的第一个为1的位置记为第n位，通过第n位是1还是0将数组分为两个子数组。

分配的标准是第n位是1还是0。

```C++
#include<iostream>
#include<vector>
#include<queue>
#include<algorithm>
using namespace std;

class Solution {
public:
	void FindNumsAppearOnce(vector<int> data, int *num1, int *num2) {
		int len = data.size();
		if (len < 2) return;
		int res = 0;
		for (int i = 0; i < len; i++) {
			res ^= data[i];
		}

		unsigned int indexOf1 = FindFirstIndexOf1(res);
		for (int j = 0; j < len; j++) {
			if (IsBit1(data[j], indexOf1))
				*num1 ^= data[j];//*num要初始化
			else
				*num2 ^= data[j];
		}
	}

	unsigned int FindFirstIndexOf1(int res) {
		int index = 0;
		//判断条件这儿是等于0，找到为1的bit
		while ( (res & 1) == 0  && index < 8 * sizeof(int) ) {//bit位应该小于int类型所能表示的范围，sizeof(int)字节
			res >>= 1;
			index++;
		}
		return index;
	}

	bool IsBit1(int num, unsigned int index) {
		num >>= index; //右移 000001 = 010000 >> 4 
		return (num & 1); //按位与
	}
};

int main() {
	Solution s;
	vector<int> num = { 2,4,3,6,3,2,5,5 };
	int a = 0, b = 0;
	int *num1 = &a, *num2 = &b;
	s.FindNumsAppearOnce(num, num1, num2);
	cout << *num1 << " " << *num2 << endl;
	system("pause");
	return 0;
}
```

# 41. 和为S的连续正数序列

题目描述

小明很喜欢数学,有一天他在做数学作业时,要求计算出9~16的和,他马上就写出了正确答案是100。但是他并不满足于此,他在想究竟有多少种连续的正数序列的和为100(至少包括两个数)。没多久,他就得到另一组连续正数和为100的序列:18,19,20,21,22。现在把问题交给你,你能不能也很快的找出所有和为S的连续正数序列? Good Luck!

输出描述:

输出所有和为S的连续正数序列。序列内按照从小至大的顺序，序列间按照开始数字从小到大的顺序

在对二维vector进行复制的时候需要注意的：不能一个元素一个元素的复制，之间用一维的vector赋值。

```C++
#include<iostream>
#include<vector>
#include<queue>
#include<algorithm>
using namespace std;

class Solution {
public:
	vector<vector<int> > FindContinuousSequence(int sum) {
		vector<vector<int> > res;
		if (sum < 3) return res;
		int small = 1, big = 2;
		int mid = (sum + 1) / 2;

		int currSum = small + big;

		while (small < mid) {
			//while (currSum < sum) {
			//	big++;
			//	currSum += big;
			//}					
			while (currSum > sum && small < mid) {
				currSum -= small;
				small++;
			}		
			if (currSum == sum) {
				vector<int> tmp;
				for (int j = small; j <= big; j++) {
					tmp.push_back(j);
				}
				res.push_back(tmp);
			}
			big++;
			currSum += big;
		}		
		return res;
	}
};

int main() {
	Solution s;
	vector<vector<int> > res;
	res = s.FindContinuousSequence(9);
	vector<int> tmp;
	for (int i = 0; i < res.size(); i++) {
		tmp = res[i];
		for (int j = 0; j < tmp.size(); j++) {
			cout << tmp[j] << " ";
		}
		cout << endl;
	}
	system("pause");
	return 0;
}
```

# 42. 和为S的两个数字

题目描述

输入一个递增排序的数组和一个数字S，在数组中查找两个数，使得他们的和正好是S，如果有多对数字的和等于S，输出两个数的乘积最小的。

输出描述:

对应每个测试案例，输出两个数，小的先输出。

同纠结乘积最小，a+b=sum,a和b越远乘积越小，而一头一尾两个指针往内靠近的方法找到的就是乘积最小的情况。如果是乘积最大的情况就是一直找到两个指针重合，每次找到一个就将之前返回的结果向量清空然后更新为新找到的。

排好序的数组，从首尾两端找。

```C++
#include<iostream>
#include<vector>
using namespace std;

class Solution {
public:
	vector<int> FindNumbersWithSum(vector<int> array, int sum) {
		vector<int> res;
		if (array.empty()) return res;
		int i = 0;
		int j = array.size() - 1;
		int num1 = array[i], num2 = array[j];

		while (num1 + num2 > sum && j > 0) {
			j--; 
			num2 = array[j];
		}
		while (num1 + num2 < sum && i < array.size() - 1) {
			i++;
			num1 = array[i];
		} 
		if (num1 + num2 == sum) {
			res.push_back(num1);
			res.push_back(num2);
		}	
		return res;
	}
};

int main() {
	Solution s;
	vector<int> num = { 1,2,4,7,11,15 };
	vector<int> res;
	res = s.FindNumbersWithSum(num,15);
	for (int i = 0; i < res.size(); i++) {		
		cout << res[i] << " ";		
	}
	cout << endl;
	system("pause");
	return 0;
}
```

# 43. 左旋转字符串

汇编语言中有一种移位指令叫做循环左移（ROL），现在有个简单的任务，就是用字符串模拟这个指令的运算结果。对于一个给定的字符序列S，请你把其循环左移K位后的序列输出。例如，字符序列S=”abcXYZdef”,要求输出循环左移3位后的结果，即“XYZdefabc”。是不是很简单？OK，搞定它！

没有简单的题，只有没想到的好算法

假设字符串abcdef，n=3，设X=abc，Y=def，所以字符串可以表示成XY，如题干，问如何求得YX。假设X的翻转为XT，XT=cba，同理YT=fed，那么YX=(XTYT)T，三次翻转后可得结果。

```C++
#include<iostream>
#include<string>
using namespace std;

class Solution {
public:
	string LeftRotateString(string str, int n) {
		//判断n
		if (n < 0) return NULL;
		if (n == 0) return str;

		string strtmp = "";
		
		strtmp = str.substr(0, n);//the first position, and count
		str.erase(0, n);
		str += strtmp;
		return str;
	}
};

/*class Solution {
public:
	string LeftRotateString(string str, int n) {
		int len = str.length();
		if (len == 0) return "";
		n = n % len;
		str += str;
		return str.substr(n, len);
	}
};*/

int main() {
	Solution s;
	string str = "abcXYZdef"; 
	cout << s.LeftRotateString(str, 9) << endl;
	system("pause");
	return 0;
}
```

# 44. 翻转单词顺序列

牛客最近来了一个新员工Fish，每天早晨总是会拿着一本英文杂志，写些句子在本子上。同事Cat对Fish写的内容颇感兴趣，有一天他向Fish借来翻看，但却读不懂它的意思。例如，“student. a am I”。后来才意识到，这家伙原来把句子单词的顺序翻转了，正确的句子应该是“I am a student.”。Cat对一一的翻转这些单词顺序可不在行，你能帮助他么？

解法：两次翻转字符串，第一步翻转句子中所有的字符串，第二步翻转每个单词字符中的顺序。

```C++
#include<iostream>
#include<string>
using namespace std;

class Solution {
public:
	string ReverseSentence(string str) {
		int len = str.length();
		if (len == 0) return "";
		Reverse(str);
		string res = "";
		int loc = 0;
		for (int i = 0; i < len; i++) {
			if (str[i] == ' ') {
				string tmp = str.substr(loc, i - loc);
				Reverse(tmp);
				res += tmp;
				res += str[i];
				loc = i + 1;
			}
			if (i == len - 1) {
				string tmp = str.substr(loc, len - loc);
				Reverse(tmp);
				res += tmp;
			}
		}
		return res;
	}

	void Reverse(string &str) {
		int len = str.length();
		for (int i = 0; i < (len + 1) / 2; i++) {
			char tmp = str[i];
			str[i] = str[len - 1 - i];
			str[len - 1 - i] = tmp;
		}
	}
};

int main() {
	Solution s;
	string str = "Wonderful"; 
	cout <<s.ReverseSentence(str) << endl;
	system("pause");
	return 0;
}

```

# 45. 扑克牌顺子

LL今天心情特别好,因为他去买了一副扑克牌,发现里面居然有2个大王,2个小王(一副牌原本是54张^_^)...他随机从中抽出了5张牌,想测测自己的手气,看看能不能抽到顺子,如果抽到的话,他决定去买体育彩票,嘿嘿！！“红心A,黑桃3,小王,大王,方片5”,“Oh My God!”不是顺子.....LL不高兴了,他想了想,决定大\小 王可以看成任何数字,并且A看作1,J为11,Q为12,K为13。上面的5张牌就可以变成“1,2,3,4,5”(大小王分别看作2和4),“So Lucky!”。LL决定去买体育彩票啦。 现在,要求你使用这幅牌模拟上面的过程,然后告诉我们LL的运气如何， 如果牌能组成顺子就输出true，否则就输出false。为了方便起见,你可以认为大小王是0。

解题思路：首先将大小王看作是0，将5个数进行排序，例如{0，1，3，4，5}，然后统计0出现的个数，相邻数字之间的间隔数，如果间隔数大于0的个数，那么不可能是连续的数字，此外还要比较相邻数字是否相等如果，相邻数字相等，说明出现对子，那么也不可能是连续的数字。

```C++
#include<iostream>
#include<vector>
using namespace std;

class Solution {
public:
	bool IsContinuous(vector<int> numbers) {
		int len = numbers.size();
		if (len == 0) return false;
		Quicksort(numbers, 0, numbers.size() - 1);

		int numberOfZeros = 0;
		int numberOfGap = 0;
		for (int i = 0; i < numbers.size(); i++)
			if (numbers[i] == 0)
				numberOfZeros++;
		
		//记录第一个非零数字的下标
		int small = numberOfZeros;
		int big = small + 1;

		while (big < len){
			if (numbers[big] == numbers[small]) return false;

			numberOfGap += numbers[big] - numbers[small] - 1;
			small = big;
			big++;
		}
		return (numberOfGap > numberOfZeros) ? false : true;
	}

	void Quicksort(vector<int> &numbers, int begin, int end) {
		if (!numbers.empty()) {
			int index = Partition(numbers, begin, end);
			if (begin < index) {
				Quicksort(numbers, begin, index - 1);
			}
			if (index < end) {
				Quicksort(numbers, index + 1, end);
			}			
		}
	}

	int Partition(vector<int> &numbers, int begin, int end) {
		int i = begin - 1;
		int x = numbers[end];
		for (int j = begin; j < end; j++) {
			if (numbers[j] <= x) {
				i++;
				swap(numbers[j], numbers[i]);
			}				
		}
		swap(numbers[i + 1], numbers[end]);
		return i + 1;
	}

	void swap(int &a, int &b) {
		int tmp = a;
		a = b;
		b = tmp;
	}
};

int main() {
	Solution s;
	vector<int> nums = { 0,1,4,3,5 };
	cout <<s.IsContinuous(nums) << endl;
	system("pause");
	return 0;
}


```

# 46. 圆圈中最后剩下的数
每年六一儿童节,牛客都会准备一些小礼物去看望孤儿院的小朋友,今年亦是如此。HF作为牛客的资深元老,自然也准备了一些小游戏。其中,有个游戏是这样的:首先,让小朋友们围成一个大圈。然后,他随机指定一个数m,让编号为0的小朋友开始报数。每次喊到m-1的那个小朋友要出列唱首歌,然后可以在礼品箱中任意的挑选礼物,并且不再回到圈中,从他的下一个小朋友开始,继续0...m-1报数....这样下去....直到剩下最后一个小朋友,可以不用表演,并且拿到牛客名贵的“名侦探柯南”典藏版(名额有限哦!!^_^)。请你试着想下,哪个小朋友会得到这份礼品呢？(注：小朋友的编号是从0到n-1)

这是著名的约瑟夫环问题。
方法一:用环形链表模拟圆圈的经典算法；方法二：分析每次被删除的数字的规律并直接计算出圆圈中最后剩下的数字。

按照《剑指Offer》上书写的，采用list的数据结构，但是list的迭代器不可以执行减法操作，所以采用vector容器。vector好像也不行哎，自己代码写错了。

环形链表，用list来构建，由于list本身不是一个环形结构，于是每当迭代器扫描到链表末尾的时候，把迭代器移动到链表的头部。

```C++
#include<iostream>
#include<list>
using namespace std;

class Solution {
public:
	int LastRemaining_Solution(int n, int m)
	{
		if (n < 1 || m < 1)
			return -1;

		list<int> number;
		for (int i = 0; i < n; i++)
			number.push_back(i);

		list<int>::iterator it = number.begin();

		while (number.size() > 1) {
			for (int i = 0; i < m - 1; i++) {//为了防止出现指向开头的迭代器出现--操作，所以i不能小于m，小于m最后一个指针指向第m+1个位置
				it++;
				if (it == number.end())
					it = number.begin();
			}
			list<int>::iterator next = ++it;
			if (next == number.end()) next = number.begin();
			--it;
			number.erase(it);
			it = next;
		}
		return *it;
	}
};

int main() {
	Solution s;
	cout <<s.LastRemaining_Solution(5,3) << endl;
	system("pause");
	return 0;
}
```

# 47. 求1+2+3+...+n
求1+2+3+...+n，要求不能使用乘除法、for、while、if、else、switch、case等关键字及条件判断语句（A?B:C）。

```C++
#include<iostream>
#include<vector>
using namespace std;

class Solution {
public:
	int Sum_Solution(int n) {
		return n * (n + 1) / 2;
	}
};

int main() {
	Solution s;
	cout <<s.Sum_Solution(10) << endl;
	system("pause");
	return 0;
}
```

# 48. 不用加减乘除做加法

用位运算，第一步，将两个数进行异或操作；第二步，按位与左移一位计算进位项；第三步，将进位项与第一步的结果进行异或操作。重复上述过程，直到进位项为0。

```C++
#include<iostream>
#include<list>
using namespace std;

class Solution {
public:
	int Add(int num1, int num2)
	{
		int sum, carry;
		do {
			sum = num1 ^ num2;
			carry = (num1 & num2) << 1;
			num1 = sum;
			num2 = carry;
		} while (num2 != 0);

		return sum;
	}
};

int main() {
	Solution s;
	cout <<s.Add(5,3) << endl;
	system("pause");
	return 0;
}
```

# 49. 把字符串转换成整数

将一个字符串转换成一个整数(实现Integer.valueOf(string)的功能，但是string不符合数字要求时返回0)，要求不能使用字符串转换整数的库函数。 数值为0或者字符串不是一个合法的数值则返回0。

输入描述:

输入一个字符串,包括数字字母符号,可以为空

输出描述:

如果是合法的数值表达则返回该数字，否则返回0

示例1

输入
```
+2147483647
    1a33
```
输出
```
2147483647
    0
```

考虑空指针NULL，空字符串，正负号，溢出等情况。

整数的最大值是`0x7FFF FFFF`，负数的最小值`0x8000 0000`

```C++
#include<iostream>
#include<string>
using namespace std;

class Solution {
public:
	int StrToInt(string str) {
		// if str的数值为0或者str的不能转换成一个合法的数值，返回零。
		int len = str.length();
		if (len == 0) return 0;
		bool flag = true;
		char tmp = str[0];
		int index = 0;
		int result = 0;

		if (tmp == '-') {
			flag = false;
			index++;
		}
		else if (tmp == '+') {
			flag = true;
			index++;
		}

		for (int i = index; i < len; i++) {
			tmp = str[i];
			if (tmp - '0' < 0 || tmp - '0'> 9)  return 0;
			result = result * 10 + tmp - '0';
		}
		if (!flag) result = 0 - result;
		return result;
	}
};

int main() {
	Solution s;
	string str = "1+23";
	cout <<s.StrToInt(str) << endl;
	system("pause");
	return 0;
}
```

# 50. 数组中重复的数字

在一个长度为n的数组里的所有数字都在0到n-1的范围内。 数组中某些数字是重复的，但不知道有几个数字是重复的。也不知道每个数字重复几次。请找出数组中任意一个重复的数字。 例如，如果输入长度为7的数组{2,3,1,0,2,5,3}，那么对应的输出是第一个重复的数字2。

可以采用排序或者哈希表的方法，或者如下这种方法：

```C++
#include<iostream>
#include<string>
using namespace std;

class Solution {
public:
	// Parameters:
	//        numbers:     an array of integers
	//        length:      the length of array numbers
	//        duplication: (Output) the duplicated number in the array number
	// Return value:       true if the input is valid, and there are some duplications in the array number
	//                     otherwise false
	bool duplicate(int numbers[], int length, int* duplication) {
		if (numbers == NULL || length < 0)
			return false;
		for (int i = 0; i < length; i++) {
			if (numbers[i] < 0 || numbers[i]>length - 1) return false;
		}

		for (int i = 0; i < length; i++) {
			while (numbers[i] != i) {
				if (numbers[i] == numbers[numbers[i]]) {
					*duplication = numbers[i];
					return true;
				}
				int tmp = numbers[i];
				numbers[i] = numbers[tmp];
				numbers[tmp] = tmp;
			}
		}
		return false;
	}
};

int main() {
	Solution s;
	int numbers[] = {1,2,2};
	int a = 3;
	int *p = &a;
	cout <<s.duplicate(numbers,3,p) << endl;
	system("pause");
	return 0;
}
```

# 51. 构建乘积数组

给定一个数组`A[0,1,...,n-1]`,请构建一个数组`B[0,1,...,n-1]`,其中B中的元素`B[i]=A[0]*A[1]*...*A[i-1]*A[i+1]*...*A[n-1]`。不能使用除法。

采用两个矩阵的方式，每一行都是`A[0,1,...,n-1]`，其中对角线元素是1。

```C++
#include<iostream>
#include<vector>
using namespace std;

class Solution {
public:
	vector<int> multiply(const vector<int>& A) {
		vector<int> B(A);
		int len = A.size();
		if (len == 0) return B;
		B[0] = 1;
		for (int i = 1; i < len; i++) {
			B[i] = B[i - 1] * A[i - 1];
		}
		int tmp = 1;
		for (int i = len - 2; i >= 0; i--) {
			tmp *= A[i + 1];
			B[i] *= tmp;
		}
		return B;
	}
};

int main() {
	Solution s;
	const vector<int> A = { 1,2,3 };
	vector<int> B;
	B = s.multiply(A);
	for(auto i : B)
		cout << i << " ";
	cout << endl;
	system("pause");
	return 0;
}
```

# 52. 正则表达式匹配

请实现一个函数用来匹配包括`.`和`*`的正则表达式。模式中的字符`.`表示任意一个字符，而`*`表示它前面的字符可以出现任意次（包含0次）。 在本题中，匹配是指字符串的所有字符匹配整个模式。例如，字符串"aaa"与模式"a.a"和"ab*ac*a"匹配，但是与"aa.a"和"ab*a"均不匹配。

首先，考虑特殊情况：
1. 两个字符串都为空，返回true
2. 当第一个字符串不空（str），而第二个字符串空了(pattern)，返回false（因为这样，就无法匹配成功了,而如果第一个字符串空了，第二个字符串非空，还是可能匹配成功的，比如第二个字符串是`a*a*a*a*`,由于`*`之前的元素可以出现0次，所以有可能匹配成功）

之后就开始匹配第一个字符，这里有两种可能：匹配成功或匹配失败。

但考虑到pattern下一个字符可能是 `*`， 这里我们分两种情况讨论：

pattern下一个字符为 `*` 或不为 `*`：

1. pattern下一个字符不为‘*’：这种情况比较简单，直接匹配当前字符。如果匹配成功，继续匹配下一个；如果匹配失败，直接返回false。注意这里的“匹配成功”，除了两个字符相同的情况外，还有一种情况，就是pattern的当前字符为‘.’,同时str的当前字符不为‘\0’。
2. pattern下一个字符为‘*’时，稍微复杂一些，因为‘*’可以代表0个或多个。这里把这些情况都考虑到：

     * 当`*`匹配0个字符时，str当前字符不变，pattern当前字符后移两位，跳过这个‘*’符号；

     * 当`*`匹配1个或多个时，str当前字符移向下一个，pattern当前字符不变。（这里匹配1个或多个可以看成一种情况，因为：当匹配一个时，由于str移到了下一个字符，而pattern字符不变，就回到了上边的情况；当匹配多于一个字符时，相当于从str的下一个字符继续开始匹配）

```C++
#include<iostream>
#include<vector>
using namespace std;

class Solution {
public:
	bool match(char* str, char* pattern)
	{
		if (*str == '\0' && *pattern == '\0') return true;
		if(*str != '\0' && *pattern == '\0') return false;
		if (*(pattern + 1) != '*') {
			if (*str == *pattern || (*str != '\0' && *pattern == '.')) //匹配任意一个字符
				return match(str + 1, pattern + 1);
			else
				return false;
		}
		else {
			if (*str == *pattern || (*str != '\0' && *pattern == '.'))
				return match(str, pattern + 2) || match(str + 1, pattern);
			else 
				return match(str, pattern + 2);
		}
		return false;
	}
};

int main() {
	Solution s;
	char str1[] = "aaa";
	char str2[] = "ab*a";
	cout << s.match(str1, str2) << endl;
	system("pause");
	return 0;
}
```

# 53. 表示数值的字符串

请实现一个函数用来判断字符串是否表示数值（包括整数和小数）。例如，字符串"+100","5e2","-123","3.1416"和"-1E-16"都表示数值。 但是"12e","1a3.14","1.2.3","+-5"和"12e+4.3"都不是。

首先，考虑第一位数字前是否是有正负号，如果正负号，字符后移一位，判断这一位是否是数字，如果不是数字，返回false。如果后面是数字，判断第二位。

如果没有正负号判断，字符串不用后移，判断第二位。

第二位的判断，可以是`E`，`e`，`.`，数字。如果是`e`，`E`和`.`后面紧跟着数字，且后面不能再出现数字之外的字符，如果后面是`'\0'`或者是字符，return false；如果是数字，继续判断后面是否是`E`，`e`，`.`，数字。这儿应该是while循环，知道遇见`'\0'`。

字符串数值格式：
`[符号]数值[.[数值]][e/E[符号]数值]`其中`[]`之间的可有可无

```C++
#include<iostream>
#include<vector>
using namespace std;

class Solution {
public:
	bool isNumeric(char* string)
	{
		if (string == NULL) return false;
		if (*string == '+' || *string == '-') {
			string++;
		}
		if (*string == '\0') return false;

		bool numeric = true;
		scanZeroToNine(&string);
		if (*string != '\0') {
			if (*string == '.') {
				string++;
				scanZeroToNine(&string);
				if (*string == 'e' || *string == 'E') {
					numeric = isExponential(&string);
				}
			}
			else if (*string == 'e' || *string == 'E') numeric = isExponential(&string);
			else numeric = false;
		}
		return numeric && *string == '\0';
	}
	//扫描字符串中数字
	void scanZeroToNine(char** string) {
		while (**string != '\0' && **string >= '0' && **string <= '9') {
			++(*string);
		}
	}
	//匹配科学记数法
	bool isExponential(char** string) {
		if (**string != 'e' && **string != 'E') return false;
		++(*string);
		if (**string == '+' || **string == '-') ++(*string);
		if (**string == '\0') return false;
		scanZeroToNine(string);
		return (**string == '\0') ? true : false;
	}

};

int main() {
	Solution s;
	char str[] = "+-5";
	cout << s.isNumeric(str) << endl;
	system("pause");
	return 0;
}
```

# 54. 字符流中第一个不重复的字符

请实现一个函数用来找出字符流中第一个只出现一次的字符。例如，当从字符流中只读出前两个字符"go"时，第一个只出现一次的字符是"g"。当从该字符流中读出前六个字符“google"时，第一个只出现一次的字符是"l"。

输出描述:

如果当前字符流没有存在出现一次的字符，返回#字符。

思路：哈希表，键值字符，值字符的位置索引

```C++
#include<iostream>
#include<vector>
using namespace std;

class Solution
{
public:
	//Insert one char from stringstream
	Solution() :index(0) {
		for (int i = 0; i < 256; ++i) {
			occurrence[i] = -1;
		}
	}
	void Insert(char ch)
	{
		if (occurrence[ch] == -1)
			occurrence[ch] = index;
		else if (occurrence[ch] >= 0)
			occurrence[ch] = -2;
		index++;
	}
	//return the first appearence once char in current stringstream
	char FirstAppearingOnce()
	{
		char ch = '#';
		int minIndex = numeric_limits<int>::max();//返回编译器允许的int型数最大值
		for (int i = 0; i < 256; i++) {
			if (occurrence[i] >= 0 && occurrence[i] < minIndex) {
				ch = (char)i;
				minIndex = occurrence[i];
			}
		}
		return ch;
	}
private:
	//occurence[i] = -1: i字符未出现;
	//occurence[i] = -2: i字符出现多次;
	//occurence[i] >= 0: 字符i只出现一次
	int occurrence[256];
	int index;//字符流中的位置
};

int main() {
	Solution s;
	char str[] = "google";
	for (int i = 0; i < 6; i++) {
		s.Insert(str[i]);
		cout << s.FirstAppearingOnce();
	}
	system("pause");
	return 0;
}


```

# 55. 链表中环的入口结点

给一个链表，若其中包含环，请找出该链表的环的入口结点，否则，输出null。

```C++
#include<iostream>
#include<vector>
using namespace std;

struct ListNode {
	int val;
	struct ListNode *next;
	ListNode(int x) :
		val(x), next(NULL) {
	}
};

class Solution {
public:
	ListNode * EntryNodeOfLoop(ListNode* pHead)
	{
		ListNode *pNode = MeetNode(pHead);
		if (pNode == NULL)
			return NULL;
		ListNode *pNode1 = pNode;
		int nodenum = 1;
		while (pNode1->next != pNode) {//计算环中结点的数量
			pNode1 = pNode1->next;
			nodenum++;
		}
		pNode1 = pHead;
		ListNode *pNode2 = pHead;
		for (int i = 0; i < nodenum; i++)
			pNode1 = pNode1->next;
		while (pNode1 != pNode2) {
			pNode1 = pNode1->next;
			pNode2 = pNode2->next;
		}
		return pNode1;
	}
	//定义快慢两个指针，找到环中的一个结点
	ListNode * MeetNode(ListNode* pHead) {
		if (pHead == NULL)
			return NULL;
		ListNode *pSlow = pHead;
		if (pSlow == NULL)
			return NULL;
		ListNode *pFast = pSlow->next;
		while (pSlow != NULL && pFast != NULL) {
			if (pSlow == pFast)
				return pFast;
			pSlow = pSlow->next;
			pFast = pFast->next;
			if (pFast != NULL)
				pFast = pFast->next;
		}
		return NULL;
	}
};

int main() {
	//Solution s;

	system("pause");
	return 0;
}
```

# 56. 删除链表中重复的结点

在一个排序的链表中，存在重复的结点，请删除该链表中重复的结点，重复的结点不保留，返回链表头指针。 例如，链表1->2->3->3->4->4->5 处理后为 1->2->5

递归方法：
```C++
#include<iostream>
#include<vector>
using namespace std;

struct ListNode {
	int val;
	struct ListNode *next;
	ListNode(int x) :
		val(x), next(NULL) {
	}
};

class Solution {
public:
	ListNode * deleteDuplication(ListNode* pHead)
	{
		if (pHead == NULL)
			return NULL;
		if (pHead != NULL && pHead->next == NULL)
			return pHead;

		ListNode *pCurrent;

		if (pHead->next->val == pHead->val) {
			pCurrent = pHead->next->next;
			while (pCurrent != NULL && pCurrent->val == pHead->val)
				pCurrent = pCurrent->next;
			return deleteDuplication(pCurrent);

		}
		else {
			pCurrent = pHead->next;
			pHead->next = deleteDuplication(pCurrent);
			return pHead;
		}
	}
};

int main() {
	//Solution s;

	system("pause");
	return 0;
}

```

# 57. 二叉树的下一个结点

给定一个二叉树和其中的一个结点，请找出中序遍历顺序的下一个结点并且返回。注意，树中的结点不仅包含左右子结点，同时包含指向父结点的指针。

情况1：如果一个结点有右子树，那么它的下一个结点是其右子树的最左边的一个结点。

情况2：如果没有右子树，如果它是父节点的左子结点，下一节点是其父节点。

情况3：如果没有右子树，且是父节点的右子结点，下一节点往上寻找，找到一个结点（它是它父节点的左子结点），返回该节点的父节点。

```C++
#include<iostream>
#include<vector>
using namespace std;

struct TreeLinkNode {
	int val;
	struct TreeLinkNode *left;
	struct TreeLinkNode *right;
	struct TreeLinkNode *next;
	TreeLinkNode(int x) :val(x), left(NULL), right(NULL), next(NULL) {

	}
};

class Solution {
public:
	TreeLinkNode * GetNext(TreeLinkNode* pNode)
	{
		if (pNode == nullptr)
			return nullptr;
		TreeLinkNode *nextNode = nullptr;
		if (pNode->right != nullptr) {
			TreeLinkNode *pRight = pNode->right;
			while (pRight->left != nullptr)
				pRight = pRight->left;
			nextNode = pRight;
		}	
		else if (pNode->next != nullptr) {
			TreeLinkNode *pCurrent = pNode;
			TreeLinkNode *pParent = pNode->next;
			while (pParent != nullptr && pParent->right == pCurrent) {
				pCurrent = pParent;
				pParent = pParent->next;
			}
			nextNode = pParent;
		}
		return nextNode;
	}
};

int main() {
	//Solution s;

	system("pause");
	return 0;
}
```

# 58. 对称的二叉树

请实现一个函数，用来判断一颗二叉树是不是对称的。注意，如果一个二叉树同此二叉树的镜像是同样的，定义其为对称的。

前序遍历，定义一个对称前序遍历。

```C++
#include<iostream>
#include<vector>
using namespace std;

struct TreeNode {
	int val;
	struct TreeNode *left;
	struct TreeNode *right;
	TreeNode(int x) :
		val(x), left(NULL), right(NULL) {
	}
};

class Solution {
public:
	bool isSymmetrical(TreeNode* pRoot)
	{
		return isSymmetrical(pRoot, pRoot);
	}

	bool isSymmetrical(TreeNode* pRoot1, TreeNode* pRoot2) {
		if (pRoot1 == NULL && pRoot2 == NULL)
			return true;
		if (pRoot1 == NULL || pRoot2 == NULL)
			return false;
		if (pRoot1->val != pRoot2->val)
			return false;
		return isSymmetrical(pRoot1->left, pRoot2->right) && isSymmetrical(pRoot1->right, pRoot2->left);
	}
};

int main() {
	//Solution s;

	system("pause");
	return 0;
}
```

# 59. 按之字形顺序打印二叉树

请实现一个函数按照之字形打印二叉树，即第一行按照从左到右的顺序打印，第二层按照从右至左的顺序打印，第三行按照从左到右的顺序打印，其他行以此类推。

栈的数据结构

需要2个栈，当处理奇数行时，先保存右子结点，然后保存到左子结点入栈，依次将元素保存到vector容器中；当处理偶数行时，先保存左子结点，然后保存右子结点到一个栈，依次将元素保存到vector容器中。

```C++
#include<iostream>
#include<vector>
#include<stack>
using namespace std;

struct TreeNode {
	int val;
	struct TreeNode *left;
	struct TreeNode *right;
	TreeNode(int x) :
		val(x), left(NULL), right(NULL) {
	}
};

class Solution {
public:
	vector<vector<int> > Print(TreeNode* pRoot) {
		vector<vector<int> > res;
		if (pRoot == NULL)
			return res;	
		stack<TreeNode *> levels[2];
		vector<int> node;
		node.push_back(pRoot->val);
		res.push_back(node);
		node.clear();
		levels[0].push(pRoot);
		TreeNode *pNode;
		while (!levels[0].empty() || !levels[1].empty()) {
			while (!levels[0].empty()) {//奇数行
				pNode = levels[0].top();
				levels[0].pop();
				if (pNode->right) {
					levels[1].push(pNode->right);
					node.push_back(pNode->right->val);
				}
				if (pNode->left) {
					levels[1].push(pNode->left);
					node.push_back(pNode->left->val);
				}
			}
			if (!node.empty()) {
				res.push_back(node);
				node.clear();
			}

			while (!levels[1].empty()) {//偶数行
				pNode = levels[1].top();
				levels[1].pop();
				if (pNode->left) {
					levels[0].push(pNode->left);
					node.push_back(pNode->left->val);
				}
				if (pNode->right) {
					levels[0].push(pNode->right);
					node.push_back(pNode->right->val);
				}
			}
			if (!node.empty()) {
				res.push_back(node);
				node.clear();
			}			
		}
		return res;
	}
};

int main() {
	//Solution s;
	system("pause");
	return 0;
}
```

# 60. 把二叉树打印成多行

从上到下按层打印二叉树，同一层结点从左至右输出。每一层输出一行。

队列，每行push的打印的时候，需要添加层数变量和运算个数变量的限制。

```C++
#include<iostream>
#include<vector>
#include<queue>
using namespace std;

struct TreeNode {
	int val;
	struct TreeNode *left;
	struct TreeNode *right;
	TreeNode(int x) :
		val(x), left(NULL), right(NULL) {
	}
};

class Solution {
public:
	vector<vector<int> > Print(TreeNode* pRoot) {
		vector<vector<int> > res;
		if (pRoot == nullptr) return res;

		queue<TreeNode *> queTree;
		queTree.push(pRoot);
		vector<int> node;
		node.push_back(pRoot->val);
		res.push_back(node);
		node.clear();

		TreeNode *pNode;
		int currentlevel = 1;
		int nextlevel = 0;

		while (!queTree.empty()) {
			pNode = queTree.front();
			queTree.pop();
			if (pNode->left) {
				queTree.push(pNode->left);
				node.push_back(pNode->left->val);
				nextlevel++;
			}
			if (pNode->right) {
				queTree.push(pNode->right);
				node.push_back(pNode->right->val);
				nextlevel++;
			}
			currentlevel--;
			if (!node.empty() && currentlevel == 0) {
				res.push_back(node);
				node.clear();
				currentlevel = nextlevel;
				nextlevel = 0;
			}
		}
		return res;
	}
};

TreeNode* initBTree(int elements[], int size)
{
	if (size < 1)
	{
		return NULL;
	}
	//动态申请size大小的指针数组
	TreeNode **nodes = new TreeNode*[size];
	//将int数据转换为TreeNode节点
	for (int i = 0; i < size; i++)
	{
		if (elements[i] == 0)
		{
			nodes[i] = NULL;
		}
		else
		{
			nodes[i] = new TreeNode(elements[i]);
		}
	}
	queue<TreeNode*> nodeQueue;
	nodeQueue.push(nodes[0]);

	TreeNode *node;
	int index = 1;
	while (index < size)
	{
		node = nodeQueue.front();
		nodeQueue.pop();
		nodeQueue.push(nodes[index++]);
		node->left = nodeQueue.back();
		nodeQueue.push(nodes[index++]);
		node->right = nodeQueue.back();
	}
	return nodes[0];
}

int main() {
	Solution s;
	int nums[] = { 8,6,10,5,7,9,11 };
	TreeNode *tree1 = initBTree(nums, 7);
	vector<vector<int> > res;
	res = s.Print(tree1);		
	system("pause");
	return 0;
}
```

# 61. 序列化二叉树

请实现两个函数，分别用来序列化和反序列化二叉树

参考

https://www.nowcoder.com/profile/9696723/codeBookDetail?submissionId=14300845

```C++
#include<iostream>
#include<queue>
#include<string>
using namespace std;

/*
空指针用#来代替，前序遍历。
*/

struct TreeNode {
	int val;
	struct TreeNode *left;
	struct TreeNode *right;
	TreeNode(int x) :
		val(x), left(NULL), right(NULL) {
	}
};

class Solution {
public:

	void TreeToStr(TreeNode *root, string &str) {
		if (root == nullptr) {
			str += '#';
			return;
		}
			
		str += to_string(root->val);
		str += ',';
		TreeToStr(root->left, str);
		TreeToStr(root->right, str);
	}

	char* Serialize(TreeNode *root) {
		if (root == nullptr)
			return nullptr;
		string str;
		TreeToStr(root, str);
		char* ret = new char[str.length() + 1];
		int i;
		for (i = 0; i < str.length(); i++) {
			ret[i] = str[i];
		}
		ret[i] = '\0';
		return ret;
	}

	TreeNode* Deserialize(char *str) {
		if (str == nullptr)
			return nullptr;
		TreeNode *ret = StrToTree(&str);
		return ret;
	}

	TreeNode * StrToTree(char **str) {
		if (**str == '#') {
			(*str)++;
			return nullptr;
		}

		int num = 0;
		while (**str != '\0' && **str != ',') {
			num = num * 10 + ((**str) - '0');
			(*str)++;
		}

		TreeNode *root = new TreeNode(num);

		if (**str == '\0')
			return root;
		else
			(*str)++;

		root->left = StrToTree(str);
		root->right = StrToTree(str);

		return root;
	}
};

TreeNode* initBTree(int elements[], int size)
{
	if (size < 1)
	{
		return NULL;
	}
	//动态申请size大小的指针数组
	TreeNode **nodes = new TreeNode*[size];
	//将int数据转换为TreeNode节点
	for (int i = 0; i < size; i++)
	{
		if (elements[i] == 0)
		{
			nodes[i] = NULL;
		}
		else
		{
			nodes[i] = new TreeNode(elements[i]);
		}
	}
	queue<TreeNode*> nodeQueue;
	nodeQueue.push(nodes[0]);

	TreeNode *node;
	int index = 1;
	while (index < size)
	{
		node = nodeQueue.front();
		nodeQueue.pop();
		nodeQueue.push(nodes[index++]);
		node->left = nodeQueue.back();
		nodeQueue.push(nodes[index++]);
		node->right = nodeQueue.back();
	}
	return nodes[0];
}

int main() {
	Solution s;
	int nums[] = { 8,6,10,5,7,9,11 };
	TreeNode *tree1 = initBTree(nums, 7);
	TreeNode *tree2 = s.Deserialize(s.Serialize(tree1));
	system("pause");
	return 0;
}
```

# 62. 二叉搜索树的第k个结点

给定一棵二叉搜索树，请找出其中的第k小的结点。例如， （5，3，7，2，4，6，8）中，按结点数值大小顺序第三小结点的值为4。

中序遍历一个二叉搜索树就可以得到一个递增排序序列，中序遍历的第k个值。

k中记录结点个数值。

```C++
#include<iostream>
#include<queue>
#include<string>
using namespace std;

/*
空指针用#来代替，前序遍历。
*/

struct TreeNode {
	int val;
	struct TreeNode *left;
	struct TreeNode *right;
	TreeNode(int x) :
		val(x), left(NULL), right(NULL) {
	}
};

class Solution {
public:
	TreeNode * KthNode(TreeNode* pRoot, int k)
	{
		if (pRoot == nullptr || k == 0)
			return nullptr;
		return MidOrder(pRoot, k);
	}

	TreeNode * MidOrder(TreeNode* pRoot, int &k) {
		TreeNode *target = nullptr;

		if (pRoot->left != nullptr)
			target = MidOrder(pRoot->left, k);

		if (target == nullptr) {
			if (k == 1)
				target = pRoot;
			k--;
		}

		if (target == nullptr && pRoot->right != nullptr){
			target = MidOrder(pRoot->right, k);
		}
		return target;
	}
};

TreeNode* initBTree(int elements[], int size)
{
	if (size < 1)
	{
		return NULL;
	}
	//动态申请size大小的指针数组
	TreeNode **nodes = new TreeNode*[size];
	//将int数据转换为TreeNode节点
	for (int i = 0; i < size; i++)
	{
		if (elements[i] == 0)
		{
			nodes[i] = NULL;
		}
		else
		{
			nodes[i] = new TreeNode(elements[i]);
		}
	}
	queue<TreeNode*> nodeQueue;
	nodeQueue.push(nodes[0]);

	TreeNode *node;
	int index = 1;
	while (index < size)
	{
		node = nodeQueue.front();
		nodeQueue.pop();
		nodeQueue.push(nodes[index++]);
		node->left = nodeQueue.back();
		nodeQueue.push(nodes[index++]);
		node->right = nodeQueue.back();
	}
	return nodes[0];
}

int main() {
	Solution s;
	int nums[] = { 8,6,10,5,7,9,11 };
	TreeNode *tree1 = initBTree(nums, 7);
	TreeNode *node = s.KthNode(tree1, 5);
	cout << node->val << endl;
	system("pause");
	return 0;
}
```

# 63. 数据流中的中位数

如何得到一个数据流中的中位数？如果从数据流中读出奇数个数值，那么中位数就是所有数值排序之后位于中间的数值。如果从数据流中读出偶数个数值，那么中位数就是所有数值排序之后中间两个数的平均值。我们使用Insert()方法读取数据流，使用GetMedian()方法获取当前读取数据的中位数。

数据的数目随着时间的增加而增加。选择的数据结构：数组、排序的链表（两个指针）、二叉搜索树（不平衡时看起来像排序的链表）->平衡的二叉搜索树（AVL）。

数据容器分为两个部分，左边部分的最大值，右边部分的最小值，即使左右两个部分没有排好序也没有关系。左边部分用最大堆实现，右边部分用最小堆实现。

在堆中插入一个数的时间O(logn)，O(1)的时间来找到堆顶的数据。

```
std::make_heap 建立堆，将[start, end)范围进行堆排序，默认使用less<int>, 即最大元素放在第一个。

std::pop_heap 将front（即第一个最大元素）移动到end的前部，同时将剩下的元素重新构造成(堆排序)一个新的heap。

std::push_heap 对刚插入尾部的元素做堆排序

std::sort_heap 将一个堆做排序，最终成为一个有序的系列，可以看到sort_heap时，必须先是一个堆（两个特性：1、最大元素在第一个 2、添加或者删除元素以对数时间），因此必须先做一次make_heap.

less 第三个参数，实现最大堆

greater 实现最小堆
```
[参考1](https://blog.csdn.net/morewindows/article/details/6967409)

[参考2](https://blog.csdn.net/morewindows/article/details/6709644)

作为一个数据结构，最好用类将其数据和方法封装起来，这样即便于操作，也便于理解。此外，除了堆排序要使用堆，另外还有很多场合可以使用堆来方便和高效的处理数据

```
容器的pop_back删除最后一个元素
```

```C++
#include<iostream>
#include<algorithm>
#include<vector>
using namespace std;

class Solution {
public:
	void Insert(int num)
	{
		if ( ((min.size() + max.size()) & 1) == 0) {//两个堆大小为偶数 括号优先级别出错
			if (max.size() > 0 && num < max[0]) {
				/*虽然现在是偶数，但是新插入的数据小于最大堆中的部分数据，
				要保证最小堆中所有的数都大于最大堆中的数
				*/
				max.push_back(num);
				push_heap(max.begin(), max.end(), less<int>());
				num = max[0];
				pop_heap(max.begin(), max.end(), less<int>());
				max.pop_back();//容器删除数据在对操作之后
			}
			min.push_back(num);
			push_heap(min.begin(), min.end(), greater<int>());
		}
		else {//应该插入最大堆，但是新插入的数据比最小堆中的部分数据还要大
			if (min.size() > 0 && num > min[0]) {
				min.push_back(num);
				push_heap(min.begin(), min.end(), greater<int>());
				num = min[0];
				pop_heap(min.begin(), min.end(), greater<int>());
				min.pop_back();//此时min[0]以及移动到了最后
			}
			max.push_back(num);
			push_heap(max.begin(), max.end(), less<int>());
		}
	}

	double GetMedian()
	{
		int size = min.size() + max.size();
		if (size <= 0)
			return 0;

		if ((size & 1) == 0)//偶数个数
			return (min[0] + max[0]) / 2.0;
		else
			return min[0];//偶数时插入最小堆，最小堆多一个
	}

private:
	vector<int> min;//最小堆
	vector<int> max;//最大堆
};

int main() {
	Solution s;
	vector<int> ins = { 1,2,3,4,5 };
	for (auto i : ins)
		s.Insert(i);
	cout << s.GetMedian() << endl;
	system("pause");
	return 0;
}
```

# 64. 滑动窗口的最大值

给定一个数组和滑动窗口的大小，找出所有滑动窗口里数值的最大值。例如，如果输入数组{2,3,4,2,6,2,5,1}及滑动窗口的大小3，那么一共存在6个滑动窗口，他们的最大值分别为{4,4,6,6,6,5}； 针对数组{2,3,4,2,6,2,5,1}的滑动窗口有以下6个： {[2,3,4],2,6,2,5,1}， {2,[3,4,2],6,2,5,1}， {2,3,[4,2,6],2,5,1}， {2,3,4,[2,6,2],5,1}， {2,3,4,2,[6,2,5],1}， {2,3,4,2,6,[2,5,1]}。

双向队列，队列中存储数组元素的下标，对头总是保存着窗口的最大值，不断向队列中添加元素，如果添加的元素大于队尾元素，删除队尾元素；如果队头元素下标大于窗口大小，删除队头元素。

```C++
#include<iostream>
#include<vector>
#include<deque>
using namespace std;

class Solution {
public:
	vector<int> maxInWindows(const vector<int>& num, unsigned int size)
	{
		vector<int> maxInWindows;
		if (num.size() >= size && size >= 1) {
			deque<int> index;
			for (int i = 0; i < size; i++) {
				while (!index.empty() && num[i] >= num[index.back()])
					index.pop_back();
				index.push_back(i);
			}

			for (int i = size; i < num.size(); i++) {
				maxInWindows.push_back(num[index.front()]);
				
				while (!index.empty() && num[i] >= num[index.back()])
					index.pop_back();
				if (!index.empty() && index.front() <= i - size)
					index.pop_front();

				index.push_back(i);
			}
			maxInWindows.push_back(num[index.front()]);
		}
		return maxInWindows;
	}
};

int main() {
	Solution s;
	const vector<int> num = { 2,3,4,2,6,2,5,1 };
	vector<int> res = s.maxInWindows(num, 3);
	for (auto i : res)
		cout << i << "";
	cout << endl;
	system("pause");
	return 0;
}
```

# 65. 矩阵中的路径

回溯法

请设计一个函数，用来判断在一个矩阵中是否存在一条包含某字符串所有字符的路径。路径可以从矩阵中的任意一个格子开始，每一步可以在矩阵中向左，向右，向上，向下移动一个格子。如果一条路径经过了矩阵中的某一个格子，则之后不能再次进入这个格子。 例如 a b c e s f c s a d e e 这样的3 X 4 矩阵中包含一条字符串"bcced"的路径，但是矩阵中不包含"abcb"路径，因为字符串的第一个字符b占据了矩阵中的第一行第二个格子之后，路径不能再次进入该格子。

```
a b c e
s f c s
a d e e
```

首先，在矩阵中任选一个格子作为路径的起点。
如果路径上的第i个字符不是ch，那么这个格子不可能处在路径上的第i个位置。
如果路径上的第i个字符正好是ch，那么往相邻的格子寻找路径上的第i+1个字符。除在矩阵边界上的格子之外，其他格子都有4个相邻的格子。
重复这个过程直到路径上的所有字符都在矩阵中找到相应的位置。

由于回朔法的递归特性，路径可以被开成一个栈。当在矩阵中定位了路径中前n个字符的位置之后，在与第n个字符对应的格子的周围都没有找到第n+1个字符，这个时候只要在路径上回到第n-1个字符，重新定位第n个字符。

由于路径不能重复进入矩阵的格子，还需要定义和字符矩阵大小一样的布尔值矩阵，用来标识路径是否已经进入每个格子。 
当矩阵中坐标为(row,col)的格子和路径字符串中相应的字符一样时，从4个相邻的格子(row,col-1),(row-1,col),(row,col+1)以及(row+1,col)中去定位路径字符串中下一个字符。
如果4个相邻的格子都没有匹配字符串中下一个的字符，表明当前路径字符串中字符在矩阵中的定位不正确，我们需要回到前一个，然后重新定位。
一直重复这个过程，直到路径字符串上所有字符都在矩阵中找到合适的位置。

```C++
#include<iostream>
#include<vector>
#include<deque>
using namespace std;

class Solution {
public:
	bool hasPath(char* matrix, int rows, int cols, char* str)
	{
		if (matrix == nullptr || rows < 1 || cols < 1 || str == nullptr)
			return false;
		bool *visited = new bool[rows*cols]();
		int pathLength = 0;
		for (int i = 0; i < rows; i++) {
			for (int j = 0; j < cols; j++) {
				if (hasPathCore(matrix, rows, cols, i, j, str, pathLength, visited))
					return true;
			}
		}
		return false;
	}

	bool hasPathCore(char *matrix, int rows, int cols, int row, int col, char *str, int &pathLength, bool *visited) {
		if (str[pathLength] == '\0')
			return true;
		bool hasPath = false;
		if (row >= 0 && row < rows && col >= 0 && col < cols && matrix[row*cols + col] == str[pathLength] && !visited[row*cols + col]) {
			++pathLength;
			visited[row*cols + col] = true;
			hasPath = hasPathCore(matrix, rows, cols, row, col + 1, str, pathLength, visited)
				|| hasPathCore(matrix, rows, cols, row, col - 1, str, pathLength, visited)
				|| hasPathCore(matrix, rows, cols, row + 1, col, str, pathLength, visited)
				|| hasPathCore(matrix, rows, cols, row - 1, col, str, pathLength, visited);
			if (!hasPath) {
				--pathLength;
				visited[row*cols + col] = false;
			}
		}
		return hasPath;
	}
};

int main() {
	Solution s;
	char matrix[] = "abcesfcsadee";
	char str[] = "abcb";
	cout << s.hasPath(matrix, 3, 4, str) << endl;
	system("pause");
	return 0;
}
```
# 66. 机器人的运动范围

地上有一个m行和n列的方格。一个机器人从坐标0,0的格子开始移动，每一次只能向左，右，上，下四个方向移动一格，但是不能进入行坐标和列坐标的数位之和大于k的格子。 例如，当k为18时，机器人能够进入方格（35,37），因为3+5+3+7 = 18。但是，它不能进入方格（35,38），因为3+5+3+8 = 19。请问该机器人能够达到多少个格子？

回溯算法：机器人从坐标(0,0)开始移动，当它准备进入坐标(i,j)的格子的时候，通过检查坐标的数位来判断机器人是否能够进入。

```C++
#include<iostream>
using namespace std;

class Solution {
public:
	int movingCount(int threshold, int rows, int cols)
	{
		bool *visited = new bool[rows*cols]();
		for (int i = 0; i < rows*cols; i++)
			visited[i] = false;
		int count = movingCountCore(threshold, rows, cols, 0, 0, visited);
		return count;
	}

	int movingCountCore(int threshold, int rows, int cols, int row, int col, bool *visited) {
		int count = 0;
		if (check(threshold, rows, cols, row, col, visited)) {
			visited[row*cols + col] = true;
			count = 1 + movingCountCore(threshold, rows, cols, row, col + 1, visited)
				+ movingCountCore(threshold, rows, cols, row, col - 1, visited)
				+ movingCountCore(threshold, rows, cols, row + 1, col, visited)
				+ movingCountCore(threshold, rows, cols, row - 1, col, visited);
		}
		return count;
	}

	bool check(int threshold, int rows, int cols, int row, int col, bool *visited) {
		if (row >= 0 && row < rows && col >= 0 && col < cols 
			&& getDigitSum(row) + getDigitSum(col) <= threshold 
			&& !visited[row*cols + col])
			return true;
		return false;
	}

	int getDigitSum(int num) {
		int sum = 0;
		while (num > 0) {
			sum += num % 10;
			num = num / 10;
		}
		return sum;
	}
};

int main() {
	Solution s;
	cout << s.movingCount(18, 3, 4);
	system("pause");
	return 0;
}
```

# 67. 剪绳子

给你一根长度为n的绳子，请把绳子剪成m段（m、n都是整数，n>1并且m>1），每段绳子的长度记为k[0],k[1],...,k[m]。请问k[0]xk[1]x...xk[m]可能的最大乘积是多少？例如，当绳子的长度是8时，我们把它剪成长度分别为2、3、3的三段，此时得到的最大乘积是18。

输入：
`n`

输出：乘积

贪心算法
-----------------------------------------------------
```C++
#include <iostream>
#include <list>
using namespace std;

int cutRope(int number) {
	if (number < 2) return 0;
	if (number == 2) return 1;
	if (number == 3) return 2;

	int timesof3 = number / 3;
	if (number - timesof3*3 == 1) timesof3--;
	
	int timesof2 = (number - timesof3 * 3) / 2;

	return (int)(pow(2, timesof2))*(int)(pow(3, timesof3));
}
int main() {
	int n;
	cin >> n;
	cout << cutRope(n) << endl;
	system("pause");
	return 0;
}
```