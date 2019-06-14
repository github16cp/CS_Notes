<!-- GFM-TOC -->
* [1. 数组](#1-数组)
* [2. 哈希表](#2-哈希表)
* [3. 链表](#3-链表)
* [4. Math](#4-Math)
* [5. 对撞指针](#5-对撞指针)
* [6. 字符串](#6-字符串)
* [7. 二分搜索](#7-二分搜索)
* [8. 分治](#8-分治)
* [9. 动态规划](#9-动态规划)
* [10. 回溯](#10-回溯)
* [11. 栈](#11-栈)
* [12. 堆](#12-堆)
* [13. 贪心算法](#13-贪心算法)
* [14. 排序](#14-排序)
* [15. 位操作](#15-位操作)
* [16. 树](#16-树)
* [17. 深度优先搜索](#17-深度优先搜索)
* [18. 广度优先搜索](#18-广度优先搜索)
* [19. 并查集UnionFind](#19-并查集UnionFind)
* [20. 图](#20-图)
* [21. 设计题Design](#21-设计题Design)
* [22. 拓扑排序](#22-拓扑排序)
* [23. 字典树Trie](#23-字典树Trie)
* [24. 树状数组BinaryIndexedTree](#24-树状数组BinaryIndexedTree)
* [25. 线段树SegmentTree](#25-线段树SegmentTree)
* [26. 二叉搜索树](#26-二叉搜索树)
* [27. 递归](#27-递归)
* [28. 脑筋急转弯Brainteaser](#28-脑筋急转弯Brainteaser)
* [29. Memoization](#29-Memoization)
* [30. 队列](#30-队列)
* [31. 极大极小值](#31-极大极小值)
* [32. 蓄水池抽样问题ReservoirSampling](#32-蓄水池抽样问题ReservoirSampling)
* [33. OrderedMap](#33-OrderedMap)
* [34. 几何题Geometry](#34-几何题Geometry)
* [35. Random](#35-Random)
* [36. 拒绝采样RejectionSampling](#36-拒绝采样RejectionSampling)
* [37. 滑动窗口](#37-滑动窗口)
* [38. LineSweep](#38-LineSweep)
* [39. 未分类](#39-未分类)
<!-- GFM-TOC -->

# 1. 数组
[array类题目](https://leetcode.com/problemset/all/?topicSlugs=array)
## 1013. Partition Array Into Three Parts With Equal Sum
```C++
//[-1,1,-1,1]
class Solution {
public:
	bool canThreePartsEqualSum(vector<int>& A) {
		int total = accumulate(A.begin(), A.end(), 0);
		if (total % 3 != 0) return false;
		int parts = 0;
		for (int i = 0, sum = 0; i < A.size() && parts < (total != 0 ? 2 : 3); ++i) {
			sum += A[i];
			if (sum == total / 3) ++parts, sum = 0;
		}
		return parts == (total != 0 ? 2 : 3);
	}
};

```
## 888. Fair Candy Swap
```C++
class Solution {
public:
	vector<int> fairCandySwap(vector<int>& A, vector<int>& B) {
		int sumA = accumulate(A.begin(), A.end(), 0);
		int sumB = accumulate(B.begin(), B.end(), 0);
		int total = (sumA + sumB) / 2;
		for (auto i : A) {
			int item = total - (sumA - i);
			for (auto j : B)
				if (j == item) return {i,item};
		}
		return {};
	}
};
```
## 448. Find All Numbers Disappeared in an Array
```C++
class Solution {
public:
	vector<int> findDisappearedNumbers(vector<int>& nums) {
		vector<int> res;
		for (int i = 0; i < nums.size(); i++) {
			int val = abs(nums[i]) - 1;
			if (nums[val] > 0) {
				nums[val] = -nums[val];
			}
		}

		for (int i = 0; i < nums.size(); i++) {
			if (nums[i] > 0) {
				res.push_back(i + 1);
			}
		}

		return res;
	}
};
```
## 717. 1-bit and 2-bit Characters
```C++
class Solution {
public:
	bool isOneBitCharacter(vector<int>& bits) {
		int ones = 0;
		for (int i = bits.size() - 2; i >= 0 && bits[i] != 0; --i) ones++;
		return ones % 2 == 0;
	}
};
```
## 999. Available Captures for Rook
```C++
class Solution {
public:
	int numRookCaptures(vector<vector<char>>& board) {
		for (int i = 0; i < board.size(); i++) 
			for (int j = 0; j < board[0].size(); j++)
				if (board[i][j] == 'R')
					return cap(board, i, j, 0, 1) + cap(board, i, j, 0, -1) + cap(board, i, j, 1, 0) + cap(board, i, j, -1, 0);
		return 0;
	}

	int cap(vector<vector<char> >& board, int x, int y, int dx, int dy) {
		while (x >= 0 && x < board.size() && y >= 0 && y < board[x].size() && board[x][y] != 'B') {
			if (board[x][y] == 'p') return 1;
			x += dx; y += dy;
		}
		return 0;
	}
};
```
## 1002. Find Common Characters
```C++
class Solution {
public:
	vector<string> commonChars(vector<string>& A) {
		vector<string> res;
		vector<int> cnt(26, INT_MAX);
		for (auto s : A) {
			vector<int> cnt_s(26, 0);
			for (auto c : s) ++cnt_s[c - 'a'];
			for (int i = 0; i < 26; i++) cnt[i] = min(cnt[i], cnt_s[i]);
		}
		for (int i = 0; i < 26; i++)
			for (int j = 0; j < cnt[i]; j++) res.push_back(string(1, i + 'a'));
		return res;
	}
};
```
## 985. Sum of Even Numbers After Queries
```C++
class Solution {
public:
	vector<int> sumEvenAfterQueries(vector<int>& A, vector<vector<int>>& queries) {
		vector<int> answer(queries.size(), 0);
		int sum = 0;
		for (auto i : A) {
			if (i % 2 == 0)
				sum += i;
		}
		//A[index]是偶数，加奇数，减去A[index]；A[index]是偶数，加偶数，加上val(减去A[index])
		for (int i = 0; i < queries.size(); i++) {
			int val = queries[i][0];
			int index = queries[i][1];
			if (A[index] % 2 == 0) {
				sum -= A[index];
			}
			A[index] = A[index] + val;
			if (A[index] % 2 == 0) {
				sum += A[index];
			}
			answer[i] = sum;
		}
		return answer;
	}
};
```
## 867. Transpose Matrix
```C++
class Solution {
public:
	vector<vector<int>> transpose(vector<vector<int>>& A) {
		int m = A.size();
		int n = A[0].size();
		vector<vector<int>> res(n, (vector<int>(m, 0)));
		for (int i = 0; i < n; i++) {
			for (int j = 0; j < m; j++) {
				res[i][j] = A[j][i];
			}
		}
		return res;
	}
};
```
## 566. Reshape the Matrix
```C++
class Solution {
public:
	vector<vector<int>> matrixReshape(vector<vector<int>>& nums, int r, int c) {
		vector<vector<int>> res(r, (vector<int>(c, 0)));
		int m = nums.size(), n = nums[0].size();
		if (r * c != m * n) return nums;
		for (int i = 0; i < r*c; i++) {
			res[i/c][i%c] = nums[i/n][i%n];
		}
		return res;
	}
};
```
## 766. Toeplitz Matrix
```C++
class Solution {
public:
	bool isToeplitzMatrix(vector<vector<int>>& matrix) {
		for (int i = 0; i < matrix.size(); i++)
			for (int j = 0; j < matrix[0].size(); j++)
				if (matrix[i][j] != matrix[i + 1][j + 1]) return false;
		return true;
	}
};
```
## 283. Move Zeroes
```C++
class Solution {
public:
	void moveZeroes(vector<int>& nums) {
		int cnt = 0;
		for (vector<int>::iterator it = nums.begin(); it != nums.end();) {
			if (*it == 0) {
				cnt++;
				it = nums.erase(it);
			}
			else it++;
		}
		for (int i = 0; i < cnt; i++)
			nums.push_back(0);
	}
};
```
## 896. Monotonic Array
```C++
class Solution {
public:
	bool isMonotonic(vector<int>& A) {
		bool inc = true, dec = true;
		for (int i = 0; i < A.size() - 1; i++)
			inc &= A[i + 1] >= A[i], dec &= A[i + 1] <= A[i];
		return inc || dec;
	}
};
```
## 485. Max Consecutive Ones
```C++
class Solution {
public:
	int findMaxConsecutiveOnes(vector<int>& nums) {
		int maxSum = INT_MIN;
		if (!nums.size()) return maxSum;
		int curSum = nums[0];
		for (int i = 1; i < nums.size(); i++) {
			if (nums[i] == nums[i - 1]) curSum += nums[i];
			else {
				if (curSum > maxSum) maxSum = curSum;
				curSum = nums[i];
			}
		}
		if (curSum > maxSum) maxSum = curSum;
		return maxSum;
	}
};
```
## 509. Fibonacci Number
```C++
class Solution {
public:
	int fib(int N) {
		if (N == 0 || N == 1) return N;
		int first = 0, second = 1, third = 0;
		for (int i = 0; i < N - 1; i++) {
			third = first + second;
			first = second;
			second = third;
		}
		return third;
	}
};
```
## 922. Sort Array By Parity II
```C++
class Solution {
public:
	vector<int> sortArrayByParityII(vector<int>& A) {
		if (!A.size()) return A;
		for (int i = 0; i < A.size(); i++) {
			if ((i % 2 == 0 && A[i] % 2 == 0) || (i % 2 != 0 && A[i] % 2 != 0)) 
				continue;
			for (int j = i + 1; j < A.size(); j++) {
				if ((i % 2 == 0 && A[j] % 2 == 0) || (i % 2 != 0 && A[j] % 2 != 0)) {
					int tmp = A[i];
					A[i] = A[j];
					A[j] = tmp;
					break;
				}
			}
		}
		return A;
	}
};
```
## 561. Array Partition I
```C++
class Solution {
public:
	int arrayPairSum(vector<int>& nums) {
		int sum = 0;
		sort(nums.begin(), nums.end());
		for (int i = 0; i < nums.size(); i += 2) {
			sum += nums[i];
		}
		return sum;
	}
};
```
## 1051. Height Checker
```C++
class Solution {
public:
	int heightChecker(vector<int>& heights) {
		int count = 0;
		vector<int> tmp(heights);
		sort(tmp.begin(), tmp.end());
		for (int i = 0; i < tmp.size(); i++) {
			if (heights[i] != tmp[i])
				count++;
		}
		return count;
	}
};
```
## 977. Squares of a Sorted Array
```C++
class Solution {
public:
	vector<int> sortedSquares(vector<int>& A) {
		for (int i = 0; i < A.size(); i++) {
			A[i] = A[i] * A[i];
		}
		sort(A.begin(), A.end());
		return A;
	}
};
```
## 832. Flipping an Image
```C++
#include <iostream>
#include <vector>
#include <string>
using namespace std;

class Solution {
public:
	vector<vector<int>> flipAndInvertImage(vector<vector<int>>& A) {
		int m = A.size();
		int n = A[0].size();
		if (m == 0) return A;
		for (int i = 0; i < m; i++) {
			reverse(A[i].begin(), A[i].end());
		}
		for (int i = 0; i < m; i++) {
			for (int j = 0; j < n; j++) {
				A[i][j] = 1 - A[i][j];
			}
		}
		return A;
	}
};

int main()
{
	Solution s;
	int m = 4;
	vector<int> tmp(m,0);
	vector<vector<int> > input;
	for (int j = 0; j < m; j++) {
		for (int i = 0; i < m; i++) {
			cin >> tmp[i];
		}
		input.push_back(tmp);
	}
	/*for (int i = 0; i < m; i++)
		for (int j = 0; j < m; j++)
			cout << input[i][j] << " ";*/
	
	vector<vector<int> > res;
	res = s.flipAndInvertImage(input);
	for (int i = 0; i < m; i++) {
		for (int j = 0; j < m; j++) {
			cout << res[i][j] << " ";
		}
		cout << endl;
	}
	system("pause");
	return 0;
}
```
## 15. 3Sum
二分查找，寻找3个数相加为0。
```C++
#include<iostream>
#include <algorithm>
#include<vector>
using namespace std;

//固定i和j,查找t,二分查找lower_bound,O(n^2*log(n))
class Solution {
public:
	vector<vector<int>> threeSum(vector<int>& nums) {
		vector<vector<int>> res;
		int len = nums.size();
		if (len == 0) return res;
		sort(nums.begin(), nums.end());
		for (int i = 0; i < len; i++) {
			for (int j = i + 1; j < len; j++) {
				vector<int> tmp;
				int t = -(nums[i] + nums[j]);
				auto it = lower_bound(nums.begin() + j + 1, nums.end(), t);//返回下标
				if (it != nums.end() && *it == t) {//二分查找找到
					tmp.push_back(nums[i]);
					tmp.push_back(nums[j]);
					tmp.push_back(*it);
					res.push_back(tmp);
				}
				while (j + 1 < len && nums[j + 1] == nums[j]) {
					j++;

				}
			}
			while (i + 1 < len && nums[i + 1] == nums[i]) {
				i++;
			}
		}
		return res;
	}
};

int main()
{
	return 0;
}
```
## 26. Remove Duplicates from Sorted Array
```C++
#include <iostream>
#include <vector>
using namespace std;

class Solution {
public:
	int removeDuplicates(vector<int>& nums) {
		int len = nums.size();
		if (len == 0) return 0;
		if (len == 1) return 1;

		for (vector<int>::iterator it = nums.begin(); (it + 1)!= nums.end(); ) {
			if (*it == *(it+1))
				nums.erase(it+1);
			else it++;
		}
		return nums.size();
	}
};

int main()
{	
	Solution ss;
	vector<int> nums = { 0,0,1,1,1,2,2,3,3,4 };
	cout << ss.removeDuplicates(nums) << endl;
	system("pause");
	return 0;
}
```
## 27. Remove Element
```C++
class Solution {
public:
	int removeElement(vector<int>& nums, int val) {
		int len = nums.size();
		if (len == 0) return 0;
		for (vector<int>::iterator it = nums.begin(); it != nums.end();) {
			if (*it == val)
				it = nums.erase(it);
			else it++;
		}
		return nums.size();
	}
};
```

## 35. Search Insert Position
```C++
class Solution {
public:
	int searchInsert(vector<int>& nums, int target) {
		int len = nums.size();
		if (len == 0) return 0;		
		if (nums[0] >= target)
			return 0;
		int i = 0;
		for (; i + 1 < len; i++) {
			if (nums[i] == target)
				return i;
			if (nums[i] < target && nums[i + 1] >= target)
				return i + 1;
		}
		return len;
	}
};
```
## 53. Maximum Subarray
```C++
class Solution {
public:
	int maxSubArray(vector<int>& nums) {
		int len = nums.size();
		if (len == 0) return 0;
		int cursum = 0;//累加的子数组的和
		int greatsum = 0x80000000;//最大的子数组的和
		for (int i = 0; i < len; i++) {
			if (cursum <= 0)
				cursum = nums[i];
			else
				cursum += nums[i];

			if (cursum > greatsum)
				greatsum = cursum;
		}
		return greatsum;
	}
};
```
## 66. Plus One
```C++
#include <iostream>
#include <vector>
using namespace std;

class Solution {
public:
	vector<int> plusOne(vector<int>& digits) {
		if (!digits.size()) return digits;
		int carry = 1;
		for (int i = digits.size() - 1; i >= 0; --i) {
			int tmp = digits[i] + carry;
			digits[i] = tmp % 10;
			carry = tmp / 10;
		}
		if (carry) digits.insert(digits.begin(), carry);
		return digits;
	}
};

int main() {
	Solution s;
	vector<int> vec = { 1,2,3 };
	vector<int> res;
	res = s.plusOne(vec);
	for (auto i : res)
		cout << i << " ";
	cout << endl;
	system("pause");
	return 0;
}
```
## 88. Merge Sorted Array
```C++
class Solution {
public:
	void merge(vector<int>& nums1, int m, vector<int>& nums2, int n) {
		if (!nums2.size()) return;
		if (!nums1.size()) return;
		if (nums1.size() < (m + n)) return;
		int j = 0;
		for (int i = m; i < nums1.size() && j < nums1.size(); ++i)
			nums1[i] = nums2[j++];
		sort(nums1.begin(), nums1.end());
	}
};
```
## 118. Pascal's Triangle
杨辉三角
```C++
class Solution {
public:
	vector<vector<int>> generate(int numRows) {
		vector<vector<int> > res;
		if (numRows == 0) return res;

		vector<int> tmp(1, 1);//第一个
		res.push_back(tmp);

		for (int i = 2; i <= numRows; i++) {
			tmp.push_back(0);
			vector<int> cur = tmp;
			for (int j = 1; j < i; j++)
				cur[j] = tmp[j] + tmp[j - 1];
			res.push_back(cur);
			tmp = cur;
		}
		return res;
	}
};
```
## 119. Pascal's Triangle II
```C++
class Solution {
public:
	vector<int> getRow(int rowIndex) {
		vector<int> res;
		if (rowIndex < 0) return res;

		vector<int> last(1,1);///rowIndex = 0
		res = last;
		for (int i = 2; i < rowIndex + 2; i++) {//rowIndex = 1;
			last.push_back(0);
			res = last;
			for (int j = 1; j < i; j++)
				res[j] = last[j] + last[j - 1];
			last = res;
		}
		return res;
	}
};
```
## 121. Best Time to Buy and Sell Stock
```C++
class Solution {
public:
	int maxProfit(vector<int>& prices) {
		int len = prices.size();
		if (len <= 1) return 0;
		int res = prices[1] - prices[0], minprice = prices[0];
		for (int i = 2; i < len; i++) {
			minprice = min(minprice, prices[i - 1]);
			if (res < prices[i] - minprice)
				res = prices[i] - minprice;
		}
		if (res < 0) return 0;
		return res;
	}
};
```
## 167. Two Sum II - Input array is sorted
```C++
class Solution {
public:
	vector<int> twoSum(vector<int>& numbers, int target) {
		if (numbers.size() == 0) return {};
		int begin = 0, end = numbers.size() - 1;
		while (begin < end) {
			int sum = numbers[begin] + numbers[end];
			if (sum == target)
				return { begin + 1,end + 1 };
			else if (sum > target) {
				end--;
			}
			else begin++;
		}
		return {};
	}
};
```
## 217. Contains Duplicate
```C++
class Solution {
public:
	bool containsDuplicate(vector<int>& nums) {
		return nums.size() > set<int>(nums.begin(), nums.end()).size();
	}
};
```
## 219. Contains Duplicate II
```C++
//set中保留距离小于等于k的不重复元素，如果元素在s中返回true，否则更新set
class Solution {
public:
	bool containsNearbyDuplicate(vector<int>& nums, int k) {
		unordered_set<int> s;
		if (k <= 0) return false;
		if (k >= nums.size()) k = nums.size() - 1;

		for (int i = 0; i < nums.size(); i++) {
			if (i > k) s.erase(nums[i - k - 1]);
			if (s.find(nums[i]) != s.end()) return true;
			s.insert(nums[i]);
		}
		return false;
	}
};
```
## 169. Majority Element
```C++
class Solution {
public:
	int majorityElement(vector<int>& nums) {
		if (nums.size() == 0) return 0;
		int res = nums[0];
		int times = 1;
		for (int i = 1; i < nums.size(); i++) {
			if (times == 0) {
				res = nums[i];
				times = 1;
			}
			else if (nums[i] == res) times++;
			else times--;
		}
		return res;
	}
};
```
## 189. Rotate Array
```C++
class Solution {
public:
	void rotate(vector<int>& nums, int k) {
		k %= nums.size();
		reverse(nums.begin(), nums.end());
		reverse(nums.begin(), nums.begin() + k);
		reverse(nums.begin() + k, nums.end());
	}
};
```
## 58. Length of Last Word
```C++
class Solution {
public:
	int lengthOfLastWord(string s) {
		int res = 0;		
		istringstream is(s);
		string laststr = "";
		while (is >> laststr) {
			res = laststr.length();
		}
		return res;
	}
};
```
## 434. Number of Segments in a String
```C++
class Solution {
public:
	int countSegments(string s) {
		int count = 0;
		istringstream is(s);
		string tmp;
		while (is >> tmp) {
			count++;
		}
		return count;
	}
};
```
## 905. Sort Array By Parity
```C++
class Solution {
public:
	vector<int> sortArrayByParity(vector<int>& A) {
		int left = 0, right = A.size() - 1;
		while (left < right) {
			if (A[left] % 2 != 0 && A[right] % 2 == 0) {
				int temp = A[left];
				A[left] = A[right];
				A[right] = temp;
				left++;
				right--;
			}
			else if (A[left] % 2 == 0) {
				left++;
			}
			else if (A[right] % 2 != 0) {
				right--;
			}			
		}
		return A;
	}
};
```
# 6. 字符串
[字符串](https://leetcode.com/problemset/all/?topicSlugs=string)
## 557. Reverse Words in a String III
```C++
class Solution {
public:
	string reverseWords(string s) {
		string res = "";
		stack<char> str;
		for (int i = 0; i < s.length(); i++) {
			if (s[i] != ' ') str.push(s[i]);
			if (s[i] == ' ') {
				while (!str.empty()) {
					res += str.top();
					str.pop();
				}
				res += ' ';
			}
		}
		while (!str.empty()) {
			res += str.top();
			str.pop();
		}
		return res;
	}
};
```

```C++
```

```C++
```
## 344. Reverse String
```C++
class Solution {
public:
	void reverseString(vector<char>& s) {
		if (s.size() == 0) return;
		int begin = 0, end = s.size() - 1;
		while (begin < end) {
			char tmp = s[begin];
			s[begin] = s[end];
			s[end] = tmp;
			begin++, end--;
		}
	}
};
```
## 151. Reverse Words in a String
用`vector<string> tmp`存，时间复杂度太高
```C++
#include<iostream>
#include<string>
#include<vector>
using namespace std;
//"  hello  world!  ";
class Solution {
public:
	string reverseWords(string s) {
		int nLength = s.length();
		if (nLength == 0) return s;
		string res = "";
		int begin, end;
		for (int i = nLength - 1; i >= 0;) {
			while (i >= 0 && s[i] == ' ') i--;
			end = i;
			if (i < 0) break;
			if (!res.empty()) res.push_back(' ');
			while (i >= 0 && s[i] != ' ') i--;
			begin = i + 1;
			res.append(s.substr(begin, end - begin + 1));
		}
		return res;
	}
};

int main()
{
	string str = "  hello  world!  ";
	Solution  s;
	cout << s.reverseWords(str) << endl;
	system("pause");
	return 0;
}

```

## 709. To Lower Case
```C++
class Solution {
public:
	string toLowerCase(string str) {
		int len = str.length();
		if (len == 0) return str;
		transform(str.begin(), str.end(), str.begin(), ::tolower);		
		return str;
	}
};
```

## 917. Reverse Only Letters
对撞指针
```C++
class Solution {
public:
	string reverseOnlyLetters(string S) {
		int left = 0;
		int right = S.size() - 1;
		while (left < right) {
			if (((S[left] >= 'A' && S[left] <= 'Z') || (S[left] >= 'a' && S[left] <= 'z')) && ((S[right] >= 'A' && S[right] <= 'Z') || (S[right] >= 'a' && S[right] <= 'z'))) {
				char tmp = S[left];
				S[left] = S[right];
				S[right] = tmp;
				left++;
				right--;
			}
			else if(!((S[left] >= 'A' && S[left] <= 'Z') || (S[left] >= 'a' && S[left] <= 'z'))){
				left++;
			}
			else {
				right--;
			}
		}
		return S;
	}
};
```


## 824. Goat Latin
```C++
class Solution {
public:
	string toGoatLatin(string S) {
		vector<string> res;
		if (!S.length()) return S;
		string tmp = "";
		for (int i = 0; i < S.length(); i++) {
			if (S[i] != ' ') tmp += S[i];
			else {
				res.push_back(tmp);
				tmp = "";
			}
		}
		res.push_back(tmp);

		int j = 0;
		for (auto i : res)
		{
			if (i[0] == 'a' || i[0] == 'e' || i[0] == 'i' || i[0] == 'o' || i[0] == 'u' || i[0] == 'A' || i[0] == 'E' || i[0] == 'I' || i[0] == 'O' || i[0] == 'U')
				i += "ma";
			else {
				string temp = "";
				if (i.length() > 1) {
					temp = i.substr(1, i.length() - 1);
					temp += i[0];
					i = temp;
				}
				i += "ma";
			}
			res[j++] = i;
		}
		j = 0;
		for (auto i : res)
		{
			int k = 0;
			while (k++ < (j + 1)) {
				i += "a";
			}
			res[j++] = i;
		}
		string result = "";
		for (auto i : res) {
			result += i;
			result += " ";
		}
		S = result.substr(0, result.length() - 1);
		return S;
	}
};
```
## 13. Roman to Integer
```C++
class Solution {
public:
	int romanToInt(string s) {		
		int res = 0;
		unordered_map<char, int> m{ {'I',1} ,{'V',5} , {'X',10} , {'L',50} , {'C',100} , {'D',500} , {'M',1000} };
		for (int i = 0; i < s.size(); i++) {
			int val = m[s[i]];
			if (i == s.size() - 1 || m[s[i + 1]] <= m[s[i]]) res += val;
			else res -= val;
		}
		return res;
	}
};
```
## 14. Longest Common Prefix
```C++
bool cmp(const string& s1, const string& s2) {
	return s1.size() < s2.size();
}

class Solution {
public:
	string longestCommonPrefix(vector<string>& strs) {
		if (strs.size() == 0) return "";
		string res = "";
		sort(strs.begin(), strs.end(), cmp);
		for (int j = 0; j < strs[strs.size() - 1].length(); j++) {
			int i = 0;
			while (i < (strs.size() - 1) && strs[i][j] == strs[i + 1][j]) i++;
			if (i == strs.size() - 1) res += strs[i][j];
			else break;
		}
		return res;
	}
};
```
## 20. Valid Parentheses
```C++
class Solution {
public:
	bool isValid(string s) {
		if (s.length() == 0) return true;
		stack<char> res;
		for (int i = 0; i < s.length(); i++) {
			if (s[i] == '(')
				res.push(')');
			else if (s[i] == '[')
				res.push(']');
			else if (s[i] == '{')
				res.push('}');
			else if (res.empty() || s[i] != res.top())
				return false;
			else res.pop();
		}
		return res.empty();
	}
};
```
## 415. Add Strings
```C++
class Solution {
public:
	string addStrings(string num1, string num2) {
		int c = 0, len1 = num1.size() - 1, len2 = num2.size() - 1;
		string res = "";
		while (c > 0 || len1 >= 0 || len2 >= 0) {
			c += len1 >= 0 ? num1[len1--] - '0' : 0;
			c += len2 >= 0 ? num2[len2--] - '0' : 0;
			res = char(c % 10 + '0')+ res;
			c /= 10;
		}
		return res;
	}
};
```

##
```C++
```


# 2. 哈希表
[哈希表](https://leetcode.com/problemset/all/?topicSlugs=hash-table)
## 136. Single Number
```C++
class Solution {
public:
	int singleNumber(vector<int>& nums) {
		if (nums.size() <= 0) return 0;
		int tmp = 0;
		for (int i = 0; i < nums.size(); i++) {
			tmp = tmp ^ nums[i];
		}
		return tmp;
	}
};
```

# 3. 链表
[链表](https://leetcode.com/problemset/all/?topicSlugs=linked-list)
## 21. Merge Two Sorted Lists
```C++
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
class Solution {
public:
	ListNode* mergeTwoLists(ListNode* l1, ListNode* l2) {
		if (l1 == nullptr) return l2;
		if (l2 == nullptr) return l1;
		ListNode* lres = nullptr;
		if (l1->val <= l2->val) {
			lres = l1;
			lres->next = mergeTwoLists(l1->next, l2);
		}
		else {
			lres = l2;
			lres->next = mergeTwoLists(l1, l2->next);
		}
		return lres;
	}
};

```
非递归方法
```C++
class Solution {
public:
	ListNode* mergeTwoLists(ListNode* l1, ListNode* l2) {
		if (l1 == nullptr) return l2;
		if (l2 == nullptr) return l1;
		ListNode head(0);
		ListNode *lres = &head;
		while (l1 != nullptr && l2 != nullptr) {
			if (l1->val <= l2->val) {
				lres->next = l1;
				l1 = l1->next;
			}
			else {
				lres->next = l2;
				l2 = l2->next;
			}
			lres = lres->next;
		}
		if (l1 != nullptr) {
			while (l1 != nullptr) {
				lres->next = l1;
				lres = lres->next;
				l1 = l1->next;
			}
		}
		else {
			while (l2 != nullptr) {
				lres->next = l2;
				lres = lres->next;
				l2 = l2->next;
			}
		}
		return head.next;
	}
};
```
## 83. Remove Duplicates from Sorted List
```C++
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
class Solution {
public:
	ListNode* deleteDuplicates(ListNode* head) {
		if (head == nullptr || head->next == nullptr) return head;
		ListNode* lres = head;
		ListNode* tmp = head->next;
		while (tmp != nullptr) {
			if (lres->val == tmp->val) {
				tmp = tmp->next;
			}
			else {
				lres->next = tmp;
				lres = tmp;
				tmp = tmp->next;
			}
		}
		lres->next = nullptr;
		return head;
	}
};
```
## 141. Linked List Cycle
```C++
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
class Solution {
public:
	bool hasCycle(ListNode *head) {
		if (head == nullptr || head->next == nullptr) return false;
		ListNode* slow = head;
		ListNode* fast = head;
		while (fast && fast->next) {
			slow = slow->next;
			fast = fast->next->next;
			if (slow == fast) return true;
		}
		return false;
	}
};
```
## 160. Intersection of Two Linked Lists
```C++
class Solution {
public:
	ListNode *getIntersectionNode(ListNode *headA, ListNode *headB) {
		if (headA == nullptr || headB == nullptr) return nullptr;
		ListNode *nodeA = headA, *nodeB = headB;
		int lenA = 0, lenB = 0;
		while (nodeA != nullptr) {
			lenA++;
			nodeA = nodeA->next;
		}
		while (nodeB != nullptr) {
			lenB++;
			nodeB = nodeB->next;
		}
		if (lenA <= lenB) {
			for (int i = 0; i < lenB - lenA; i++) {
				headB = headB->next;
			}
		}
		else {
			for (int i = 0; i < lenA - lenB; i++) {
				headA = headA->next;
			}
		}
		while (headA != headB && headA != nullptr && headB != nullptr) {
			headA = headA->next;
			headB = headB->next;
		}
		if (headA != nullptr && headB != nullptr) return headA;
		else return nullptr ;
	}
};
```
## 203. Remove Linked List Elements
```C++
class Solution {
public:
	ListNode* removeElements(ListNode* head, int val) {
		if (head == nullptr) return head;
		while (head->val == val) {
			head = head->next;
			if (head == nullptr) return head;
		}
		ListNode *ptr = head;
		while (ptr->next!= nullptr)
		{
			if (ptr->next->val == val) {
				ptr->next = ptr->next->next;
			}
			else {
				ptr = ptr->next;
			}
		}
		return head;
	}
};
```
## 206. Reverse Linked List
```C++
class Solution {
public:
	ListNode* reverseList(ListNode* head) {
		ListNode *res = nullptr;
		ListNode *curNode = head;
		ListNode *preNode = nullptr;
		while (curNode != nullptr) {
			ListNode *nextNode = curNode->next;
			if (nextNode == nullptr) res = curNode;
			curNode->next = preNode;
			preNode = curNode;
			curNode = nextNode;
		}
		return res;
	}
};
```
## 234. Palindrome Linked List
```C++
#include <iostream>
#include <string>
#include <stack>
using namespace std;

struct ListNode
{	
	int val;
	ListNode *next;
	ListNode(int x) :val(x), next(NULL) {}
};

class Solution {
public:
	ListNode* reverse(ListNode *head) {
		ListNode *res = nullptr;
		ListNode *curNode = head;
		ListNode *preNode = nullptr;
		while (curNode != nullptr) {
			ListNode *nextNode = curNode->next;
			curNode->next = preNode;
			if (nextNode == nullptr) res = curNode;
			preNode = curNode;
			curNode = nextNode;
		}
		return res;
	}
	bool isPalindrome(ListNode* head) {
		if (head == nullptr) return true;
		ListNode *ptr = head;
		int len = 0;
		while (ptr != nullptr) {
			ptr = ptr->next;
			len++;
		}		
		if (len % 2 == 0) {
			len /= 2;			
		}
		else {
			len = len / 2 + 1;
		}
		ptr = head;
		while (len > 1) {
			ptr = ptr->next;
			len--;
		}
		ListNode *head2 = ptr->next;
		ptr->next = nullptr;
		head2 = reverse(head2);
		while (head2 != nullptr) {
			if (head2->val != head->val) return false;
			head = head->next;
			head2 = head2->next;
		}
		return true;
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
	ListNode *list1;
	list1 = Creat_LinkList_R();
	cout << s.isPalindrome(list1) << endl;
	system("pause");
	return 0;
}
```
## 237. Delete Node in a Linked List
```C++
class Solution {
public:
	void deleteNode(ListNode* node) {
		*node = *(node->next);
	}
};
```

```C++
class Solution {
public:
	void deleteNode(ListNode* node) {
		ListNode *tmp = node->next;
        *node = *tmp;
        delete tmp;
	}
};
```

## 707. Design Linked List
```C++
class MyLinkedList {
public:
	class MyLinkedListNode {
	public:
		int val;
		MyLinkedListNode* next = nullptr;
		MyLinkedListNode* prev = nullptr;
		MyLinkedListNode() :val{ 0 }, next{ nullptr }, prev{ nullptr } {};
	};

	MyLinkedListNode* root = nullptr;
	/** Initialize your data structure here. */
	MyLinkedList() {
		MyLinkedListNode* root{};
	}

	/** Get the value of the index-th node in the linked list. If the index is invalid, return -1. */
	int get(int index) {
		if (index < 0)
			return -1;
		MyLinkedListNode* tmp = root;
		if (tmp == nullptr) return -1;
		for (int i = 0; i < index; i++) {
			if (tmp->next != nullptr)
				tmp = tmp->next;
			else
				return -1;
		}
		return tmp->val;
	}

	/** Add a node of value val before the first element of the linked list. After the insertion, the new node will be the first node of the linked list. */
	void addAtHead(int val) {
		MyLinkedListNode* newhead = new MyLinkedListNode();
		newhead->val = val;
		newhead->next = root;
		if (root != nullptr)
			root->prev = newhead;
		root = newhead;
	}

	/** Append a node of value val to the last element of the linked list. */
	void addAtTail(int val) {
		MyLinkedListNode* tail = root;
		while (tail != nullptr && tail->next != nullptr)
			tail = tail->next;
		MyLinkedListNode* newtail = new MyLinkedListNode();
		newtail->val = val;
		if (tail != nullptr)
			tail->next = newtail;
		else
			tail = newtail;
		newtail->prev = tail;
	}

	/** Add a node of value val before the index-th node in the linked list. If index equals to the length of linked list, the node will be appended to the end of linked list. If index is greater than the length, the node will not be inserted. */
	void addAtIndex(int index, int val) {
		if (index <= 0) {
			addAtHead(val);
			return;
		}
		if (get(index - 1) != -1) {
			MyLinkedListNode* previous = root;
			MyLinkedListNode* newone = new MyLinkedListNode();
			newone->val = val;
			for (int i = 0; i < index - 1; i++)
			{
				previous = previous->next;
			}
			newone->prev = previous;
			newone->next = previous->next;
			if (previous->next != nullptr)
				previous->next->prev = newone;
			previous->next = newone;
			return;
		}
		else return;
	}

	/** Delete the index-th node in the linked list, if the index is valid. */
	void deleteAtIndex(int index) {
		if (index < 0) return;
		if (get(index) != -1) {
			MyLinkedListNode* tmp = root;
			for (int i = 0; i < index; i++) {
				tmp = tmp->next;
			}
			if (tmp->prev != nullptr)
				tmp->prev->next = tmp->next;
			if (tmp->next != nullptr)
				tmp->next->prev = tmp->prev;

			if (index == 0)
				root = tmp->next;
			return;
		}
		else return;
	}
};

int main() {
	MyLinkedList linkedList;
	linkedList.addAtHead(7);
	linkedList.addAtHead(2);
	linkedList.addAtHead(1);
	linkedList.addAtIndex(3, 0);  // linked list becomes 1->2->3
	linkedList.deleteAtIndex(2);  // now the linked list is 1->3
	linkedList.addAtHead(6);
	linkedList.addAtTail(4);
	linkedList.get(4);            // returns 2
	linkedList.addAtHead(4);
	linkedList.addAtIndex(5, 0);  // linked list becomes 1->2->3
	linkedList.addAtHead(6);
	system("pause");
	return 0;
}
```

## 876. Middle of the Linked List
```C++
#include <iostream>
#include <string>
#include <stack>
using namespace std;

struct ListNode {
	int val;
	ListNode* next;
	ListNode(int x) :val(x),next(nullptr) {}
};

class Solution {
public:
	ListNode* middleNode(ListNode* head) {
		if (head == nullptr) return head;
		ListNode *ptr = head;
		int cnt = 0;
		while (ptr != nullptr) {
			cnt++;
			ptr = ptr->next;
		}
		if (cnt % 2 == 1) {
			cnt = cnt / 2 + 1;
		}
		else {
			cnt = cnt / 2 + 1;
		}
		ptr = head;
		while (cnt > 1) {
			ptr = ptr->next;
			cnt--;
		}
		return ptr;
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
	ListNode *list1;
	list1 = Creat_LinkList_R();
	ListNode *res;
	res = s.middleNode(list1);
	system("pause");
	return 0;
}
```

# 4. Math
[Math](https://leetcode.com/problemset/all/?topicSlugs=math)
## 942. DI String Match
```C
class Solution {
public:
	vector<int> diStringMatch(string S) {
		int left = count(S.begin(), S.end(), 'D'), right = left;
		vector<int> res = { left };
		for (auto &c : S) {
			int num = (c == 'I') ? ++right : --left;
			res.push_back(num);
		}
		return res;
	}
};
```
## 728. Self Dividing Numbers
```C++
class Solution {
public:
	vector<int> selfDividingNumbers(int left, int right) {
		vector<int> res;
		for (int i = left; i <= right; i++) {
			int j = i;
			for (; j > 0; j /= 10) {
				if ((j % 10 == 0) || (i % (j % 10) != 0)) break;
			}
			if (j == 0) res.push_back(i);
		}
		return res;
	}
};
```
## 67. Add Binary
```C++
class Solution {
public:
	string addBinary(string a, string b) {
		string res = "";
		int carry = 0, index_a = a.length() - 1, index_b = b.length() - 1;
		while (carry > 0 || index_a >= 0 || index_b >= 0) {
			carry += index_a >= 0 ? a[index_a--] - '0' : 0;
			carry += index_b >= 0 ? b[index_b--] - '0' : 0;
			res = char(carry % 2 + '0') + res;
			carry /= 2;
		}
		return res;
	}
};
```
## 69. Sqrt(x)
```C++
class Solution {
public:
	int mySqrt(int x) {
		long r = x;
		while (r*r > x) {
			r = (r + x / r) / 2;
		}
		return r;
	}
};
```
## 204. Count Primes
```C++
class Solution {
public:
	int countPrimes(int n) {
		vector<bool> notPrime(n);
		int count = 0;
		for (int i = 2; i < n; i++) {
			if (notPrime[i] == false) {
				count++;
				for (int j = 2; i*j < n; j++) {
					notPrime[i*j] = true;
				}
			}
		}
		return count;
	}
};
```
## 231. Power of Two
```C++
//位操作，如果一个数是2的幂，其2进制表示位置只有最高位1，则(n&(n - 1)) == 0
class Solution {
public:
	bool isPowerOfTwo(int n) {
		if (n <= 0) return false;
		return !(n&(n - 1));
	}
};
```
# 5. 对撞指针
[Two Pointers](https://leetcode.com/problemset/all/?topicSlugs=two-pointers)
## 125. Valid Palindrome
```C++
class Solution {
public:
	bool isPalindrome(string s) {
		if (s.length() == 0) return true;
		int left = 0, right = s.length() - 1;
		while (left < right) {
			if (s[left] == s[right] || s[left] == tolower(s[right]) || s[left] == toupper(s[right])) {
				left++;
				right--;
			}
			else if (!(s[left] >= 'a' && s[left] <= 'z') && !(s[left] >= 'A' && s[left] <= 'Z') && !(s[left] >= '0' && s[left] <= '9')) {
				left++;
			}
			else if (!(s[right] >= 'a' && s[right] <= 'z') && !(s[right] >= 'A' && s[right] <= 'Z') && !(s[right] >= '0' && s[right] <= '9')) {
				right--;
			}
			else return false;
		}
		return true;
	}
};
```
## 345. Reverse Vowels of a String
```C++
class Solution {
public:
	string reverseVowels(string s) {
		if (s.length() == 0) return "";
		int left = 0, right = s.length() - 1;
		while (left < right) {
			if ((s[left] == 'a' || s[left] == 'e' || s[left] == 'i' || s[left] == 'o' || s[left] == 'u' ||
				s[left] == 'A' || s[left] == 'E' || s[left] == 'I' || s[left] == 'O' || s[left] == 'U')
				&& (s[right] == 'a' || s[right] == 'e' || s[right] == 'i' || s[right] == 'o' || s[right] == 'u'
					|| s[right] == 'A' || s[right] == 'E' || s[right] == 'I' || s[right] == 'O' || s[right] == 'U')) {
				char tmp = s[left];
				s[left] = s[right];
				s[right] = tmp;
				left++;
				right--;
			}
			else if (!(s[left] == 'a' || s[left] == 'e' || s[left] == 'i' || s[left] == 'o' || s[left] == 'u' ||
				s[left] == 'A' || s[left] == 'E' || s[left] == 'I' || s[left] == 'O' || s[left] == 'U')) {
				left++;
			}
			else if (!(s[right] == 'a' || s[right] == 'e' || s[right] == 'i' || s[right] == 'o' || s[right] == 'u'
				|| s[right] == 'A' || s[right] == 'E' || s[right] == 'I' || s[right] == 'O' || s[right] == 'U')) {
				right--;
			}
			else {
				right--;
				left++;
			}
		}
		return s;
	}
};
```

# 7. 二分搜索
[二分搜索](https://leetcode.com/problemset/all/?topicSlugs=binary-search)

## 278. First Bad Version
```C++
bool isBadVersion(int version);

class Solution {
public:
	int firstBadVersion(int n) {
		int start = 0, end = n;
		while (end - start > 1) {
			int mid = start + (end - start) / 2;
			if (isBadVersion(mid)) end = mid;
			else start = mid;
		}
		return end;
	}
};
```
## 349. Intersection of Two Arrays
```C++
//将第二个数组排序，二分查找第一个元素是否在第二个中
class Solution {
public:
	vector<int> intersection(vector<int>& nums1, vector<int>& nums2) {
		unordered_set<int> res;
		sort(nums2.begin(), nums2.end());
		for (auto i : nums1) {
			if (binarySearch(nums2, i)) {
				res.insert(i);
			}
		}
		return vector<int>(res.begin(), res.end());
	}
	bool binarySearch(vector<int>& nums, int target) {
		int left = 0, right = nums.size() - 1;
		while (left <= right) {
			int mid = left + (right - left) / 2;
			if (nums[mid] == target) return true;
			else if (nums[mid] > target) right = mid - 1;
			else left = mid + 1;
		}
		return false;
	}
};
```
## 350. Intersection of Two Arrays II
先给两个数组排序，然后用两个指针分别指向两个数组的起始位置，如果两个指针指的数字相等，则存入结果中，两个指针均自增1，如果第一个指针指的数字大，则第二个指针自增1，反之亦然。
```C++
class Solution {
public:
	vector<int> intersect(vector<int>& nums1, vector<int>& nums2) {
		vector<int> res;
		if (nums1.size() == 0 || nums2.size() == 0) return res;
		sort(nums1.begin(), nums1.end());
		sort(nums2.begin(), nums2.end());
		int i = 0, j = 0;
		while (i < nums1.size() && j < nums2.size()) {
			if (nums1[i] == nums2[j]) {
				res.push_back(nums1[i]);
				i++;
				j++;
			} 
			else if (nums1[i] < nums2[j]) {
				i++;
			}
			else {
				j++;
			}
		}
		return res;
	}	
};
```

# 8. 分治
[分治](https://leetcode.com/problemset/all/?topicSlugs=divide-and-conquer)


```C++

```
# 9. 动态规划
[动态规划](https://leetcode.com/problemset/all/?topicSlugs=dynamic-programming)
## 70. Climbing Stairs
```C++
class Solution {
public:
	int climbStairs(int n) {
		if (n == 0) return 0;
		if (n == 1) return 1;
		if (n == 2) return 2;
		vector<int> res(n, -1);
		res[0] = 1;
		res[1] = 2;
		int num = dp(res, n - 1);
		return num;
	}
	int dp(vector<int> &res, int n) {
		if (res[n] == -1)
			res[n] = dp(res, n - 1) + dp(res, n - 2); 
		return res[n];
	}
};
```
## 64. Minimum Path Sum
```C++
class Solution {
public:
	int minPathSum(vector<vector<int>>& grid) {
		int m = grid.size();
		int n = grid[0].size();
		vector<vector<int>> sum(m, vector<int>(n, grid[0][0]));
		for (int i = 1; i < m; i++)
			sum[i][0] = sum[i - 1][0] + grid[i][0];
		for (int j = 1; j < n; j++)
			sum[0][j] = sum[0][j - 1] + grid[0][j];
		for (int i = 1; i < m; i++)
			for (int j = 1; j < n; j++)
				sum[i][j] = min(sum[i][j - 1], sum[i - 1][j]) + grid[i][j];
		return sum[m - 1][n - 1];
	}
};
```
[参考](https://leetcode.com/problems/minimum-path-sum/discuss/23457/C%2B%2B-DP)

# 10. 回溯
[回溯](https://leetcode.com/problemset/all/?topicSlugs=backtracking)
## 784. Letter Case Permutation
```C++
class Solution {
public:
	vector<string> letterCasePermutation(string S) {
		vector<string> res;
		trackback(S, 0, res);
		return res;

	}
	void trackback(string &s, int i, vector<string> &res) {
		if (i == s.size()) {
			res.push_back(s);
			return;
		}
		char c = s[i];
		s[i] = islower(c) ? toupper(c) : tolower(c);
		trackback(s, i + 1, res);
		if (isalpha(c)) {
			s[i] = c;
			trackback(s, i + 1, res);
		}
	}
};
```
# 11. 栈
[栈](https://leetcode.com/problemset/all/?topicSlugs=stack)
## 1021. Remove Outermost Parentheses
```C++
class Solution {
public:
	string removeOuterParentheses(string S) {
		string res = "";
		int opened = 0;
		for (auto c : S) {
			if (c == '(' && opened++ > 0) res += c;
			if (c == ')' && opened-- > 1) res += c;
		}
		return res;
	}
};
```
## 1047. Remove All Adjacent Duplicates In String
```C++
class Solution {
public:
	string removeDuplicates(string S) {
		if (!S.length()) return S;
		string results = "";
		stack<char> res;
		res.push(S[0]);
		for (int i = 1; i < S.length(); i++) {
			if (res.empty()) res.push(S[i]);
			else if (S[i] == res.top()) res.pop();
			else res.push(S[i]);
		}
		while (!res.empty()) {
			results += res.top();
			res.pop();
		}
		reverse(results.begin(), results.end());
		return results;
	}
};
```
# 12. 堆

# 13. 贪心算法
[贪心](https://leetcode.com/problemset/all/?topicSlugs=greedy)
## 455. Assign Cookies
```C++
class Solution {
public:
	int findContentChildren(vector<int>& g, vector<int>& s) {
		if (!g.size() || !s.size()) return 0;
		sort(g.begin(), g.end());
		sort(s.begin(), s.end());
		vector<int>::iterator it = s.begin();
		int res = 0;
		int i = 0;
		while (i < g.size()) {
			if (it == s.end()) break;
			if (g[i] <= *it) {
				res++;
				it = s.erase(it);
				i++;
			}
			else {
				it = s.erase(it);
			}
		}
		//for (int i = 0; i < g.size(); i++) {
			
			/*else {
				int sum = *it;
				it = s.erase(it);
				while (it != s.end() && g[i] > sum) {
					sum += *it;
					it = s.erase(it);
				}
				if (g[i] <= sum) res++;
			}*/
		//}
		return res;
	}
};
```
# 14. 排序
[排序](https://leetcode.com/problemset/all/?topicSlugs=sort)
# 15. 位操作
[位操作](https://leetcode.com/problemset/all/?topicSlugs=bit-manipulation)

[总结](https://leetcode.com/problems/sum-of-two-integers/discuss/84278/A-summary%3A-how-to-use-bit-manipulation-to-solve-problems-easily-and-efficiently)
## 190. Reverse Bits
```C++
//运算符&优先级低于<<高于=
class Solution {
public:
	uint32_t reverseBits(uint32_t n) {
		n = (n << 16) | (n >> 16);
		n = (n & 0x00ff00ff) << 8 | (n & 0xff00ff00) >> 8;
		n = (n & 0x0f0f0f0f) << 4 | (n & 0xf0f0f0f0) >> 4;
		n = (n & 0x33333333) << 2 | (n & 0xcccccccc) >> 2;
		n = (n & 0x55555555) << 1 | (n & 0xaaaaaaaa) >> 1;
		return n;
	}
};
```
## 191. Number of 1 Bits
```C++
class Solution {
public:
	int hammingWeight(uint32_t n) {
		int count = 0;
		while (n) {
			count++;
			n = n & (n - 1);
		}
		return count;
	}
};
```
## 268. Missing Number
```C++
class Solution {
public:
	int missingNumber(vector<int>& nums) {
		if (nums.size() == 0) return -1;
		sort(nums.begin(), nums.end());
		for (int i = 0; i < nums.size(); i++) {
			if (nums[i] != i) return i;
		}
		return nums.size();
	}
};
```
## 389. Find the Difference
```C++
class Solution {
public:
	char findTheDifference(string s, string t) {
		sort(s.begin(), s.end());
		sort(t.begin(), t.end());
		for (int i = 0; i < s.size(); i++) {
			if (t[i] != s[i]) return t[i];
		}
		return t[t.size()-1];
	}
};
```
## 461. Hamming Distance
```C++
class Solution {
public:
	int hammingDistance(int x, int y) {
		return numberOf1(x^y);
	}
	int numberOf1(int n) {
		int count = 0;
		while (n) {
			count++;
			n = n & (n - 1);
		}
		return count;
	}
};
```

```C++

```
## 338. Counting Bits
```C++
class Solution {
public:
    vector<int> countBits(int num) {
        vector<int> res;
        for(int i = 0;i <= num; i++){
            res.push_back(NumberOf1(i));
        }
        return res;
    }
    
    int NumberOf1(int num){
        int count = 0;
        while(num){
            count++;
            num = num & (num - 1);
        }
        return count;
    }
};
```
## 342. Power of Four
```C++
//(num & num - 1) == 0只有最高位为1,0x55555555保证只有奇数为1的情况下才能为4的幂，负责可能是2的幂
class Solution {
public:
	bool isPowerOfFour(int num) {
		return num > 0 && (num & num-1) == 0 && (num & 0x55555555) != 0;
	}
};

```

```C++
class Solution {
public:
	int getSum(int a, int b) {
		if (b == 0) return a;
		/*int sum = a;
		while (b != 0) {
			sum = a ^ b;
			b = (a&b) << 1;//进位
			a = sum;
		}
		return sum;*/
		//return getSum(a^b, (a&b) << 1);
		if (b == 0) return a;
		return getSum(a^b, ((a & b) & 0xffffffff) << 1);// limited to 32 bits，解决负数溢出问题
	}
};
```
# 16. 树
[树](https://leetcode.com/problemset/all/?topicSlugs=tree)
## 1022. Sum of Root To Leaf Binary Numbers
```C++
class Solution {
public:
	int sumRootToLeaf(TreeNode* root, int val = 0) {
		if (root == nullptr) return 0;
		val = (val * 2) + root->val;
		return root->left == root->right ? val : sumRootToLeaf(root->left, val) + sumRootToLeaf(root->right, val);
	}
};
```
## 637. Average of Levels in Binary Tree
```C++
class Solution {
public:
	vector<double> averageOfLevels(TreeNode* root) {
		vector<double> res;
		if (root == nullptr) return res;
		queue<TreeNode*> tree;
		tree.push(root);
		while (!tree.empty()) {
			long temp = 0;
			int s = tree.size();
			for (int i = 0; i < s; i++) {
				TreeNode* node = tree.front();
				tree.pop();
				if (node->left) tree.push(node->left);
				if (node->right) tree.push(node->right);
				temp += node->val;
			}
			res.push_back((double)temp / s);
			temp = 0;
		}
        return res;
	}
};
```
# 17. 深度优先搜索
[深度优先搜索](https://leetcode.com/problemset/all/?topicSlugs=depth-first-search)
## 257. Binary Tree Paths
```C++
class Solution {
public:
	vector<string> binaryTreePaths(TreeNode* root) {
		vector<string> res;
		if (root == nullptr) return res;
		stack<TreeNode*> s;
		stack<string> path;
		s.push(root);
		path.push(to_string(root->val));
		while (!s.empty()) {
			TreeNode* node = s.top();
			s.pop();
			string pathtmp = path.top();
			path.pop();

			if (node->left == nullptr && node->right == nullptr) {
				res.push_back(pathtmp);
				continue;
			}

			if (node->left) {
				s.push(node->left);
				path.push(pathtmp + "->" + to_string(node->left->val));
			}

			if (node->right) {
				s.push(node->right);
				path.push(pathtmp + "->" + to_string(node->right->val));
			}			
		}
	}
};
```
# 18. 广度优先搜索
[广度优先搜索](https://leetcode.com/problemset/all/?topicSlugs=breadth-first-search)
## 993. Cousins in Binary Tree
```C++
class Solution {
public:
	bool isCousins(TreeNode* root, int x, int y) {
		if (root == nullptr) return false;
		queue<TreeNode*> tree;
		tree.push(root);
		while (!tree.empty()) {
			int size = tree.size();
			bool existX = false;
			bool existY = false;
			for (int i = 0; i < size; i++) {
				TreeNode* node = tree.front();
				tree.pop();
				if (node->val == x)
					existX = true;
				if (node->val == y)
					existY = true;
				if (node->left && node->right) {
					if (node->left->val == x && node->right->val == y)
						return false;
					if (node->right->val == x && node->left->val == y)
						return false;
				}				
				if (node->left) tree.push(node->left);
				if (node->right) tree.push(node->right);
			}
			if (existX && existY) return true;
		}
		return false;
	}
};
```
## 690. Employee Importance
本地测试通过，但是AC不了，不知道原因在哪？
```C++
class Solution {
public:
	int getImportance(vector<Employee*> employees, int id) {		
		int res = 0;
		int size = employees.size();
		if (size == 0) return 0;
		sort(employees.begin(), employees.end());
		queue<int> sub;
		sub.push(id);
		for (auto i : employees) {
			int nowid = sub.front();
			if (i->id == nowid) {
				res += i->importance;
				if (i->subordinates.size()) {
					for (auto j : i->subordinates)
						sub.push(j);
				}
				sub.pop();
			}		
		}
		return res;
	}
};
```
估计方法不对，加了cmp也不对
```C++
bool cmp(Employee* a, Employee* b) {
	return a->id < b->id;
}

class Solution {
public:
	int getImportance(vector<Employee*> employees, int id) {		
		int res = 0;
		int size = employees.size();
		if (size == 0) return 0;
		sort(employees.begin(), employees.end(),cmp);
		queue<int> sub;
		sub.push(id);
		for (auto i : employees) {
			int nowid = sub.front();
			if (i->id == nowid) {
				res += i->importance;
				if (i->subordinates.size()) {
					for (auto j : i->subordinates)
						sub.push(j);
				}
				sub.pop();
			}		
		}
		return res;
	}
};
```
AC版本
```C++
class Solution {
public:
	int getImportance(vector<Employee*> employees, int id) {		
		unordered_map<int, Employee*> employee;

		for (const auto em : employees) {
			employee[em->id] = em;
		}
		return computeImportance(employee, id);
	}
	int computeImportance(unordered_map<int, Employee*>& employee, const int id) {
		int sum = employee[id]->importance;
		for (const auto em : employee[id]->subordinates) {
			sum += computeImportance(employee, em);
		}
		return sum;
	}
};
```
# 19. 并查集UnionFind
[并查集](https://leetcode.com/problemset/all/?topicSlugs=union-find)
# 20. 图
[图](https://leetcode.com/problemset/all/?topicSlugs=graph)
# 21. 设计题Design
[Design](https://leetcode.com/problemset/all/?topicSlugs=design)
# 22. 拓扑排序
[拓扑排序](https://leetcode.com/problemset/all/?topicSlugs=topological-sort)
# 23. 字典树Trie
[字典树](https://leetcode.com/problemset/all/?topicSlugs=trie)
# 24. 树状数组BinaryIndexedTree
[树状数组](https://leetcode.com/problemset/all/?topicSlugs=binary-indexed-tree)
# 25. 线段树SegmentTree
[线段树](https://leetcode.com/problemset/all/?topicSlugs=segment-tree)
# 26. 二叉搜索树
[二叉搜索树](https://leetcode.com/problemset/all/?topicSlugs=binary-search-tree)
# 27. 递归
[递归](https://leetcode.com/problemset/all/?topicSlugs=recursion)
# 28. 脑筋急转弯Brainteaser
[Brainteaser](https://leetcode.com/problemset/all/?topicSlugs=brainteaser)
# 29. Memoization
[Memoization](https://leetcode.com/problemset/all/?topicSlugs=memoization)
[参考](https://blog.csdn.net/feeltouch/article/details/45072725)
是一种将`函数返回值缓存起来`的方法，Memoization 原理非常简单，就是把函数的每次执行结果都放入一个键值对或者数组中，在接下来的执行中，在键值对中查找是否已经有相应执行过的值，如果有，直接返回该值，没有执行函数体的求值部分。很明显找值尤其是在键值对中找值，比执行函数快多了。[参考](https://blog.csdn.net/feeltouch/article/details/45072725)

# 30. 队列
[队列](https://leetcode.com/problemset/all/?topicSlugs=queue)
# 31. 极大极小值
[Minimax](https://leetcode.com/problemset/all/?topicSlugs=minimax)
# 32. 蓄水池抽样问题ReservoirSampling
[蓄水池抽样问题](https://leetcode.com/problemset/all/?topicSlugs=reservoir-sampling)
# 33. OrderedMap
[OrderedMap](https://leetcode.com/problemset/all/?topicSlugs=ordered-map)
# 34. 几何题Geometry
[几何](https://leetcode.com/problemset/all/?topicSlugs=geometry)
# 35. Random
[Random](https://leetcode.com/problemset/all/?topicSlugs=random)
# 36. 拒绝采样RejectionSampling
[拒绝采样](https://leetcode.com/problemset/all/?topicSlugs=rejection-sampling)
# 37. 滑动窗口
[滑动窗口](https://leetcode.com/problemset/all/?topicSlugs=sliding-window)
# 38. LineSweep
[扫描线算法](https://leetcode.com/problemset/all/?topicSlugs=line-sweep)

# 39. 未分类
## 771. Jewels and Stones
```C++
class Solution {
public:
	int numJewelsInStones(string J, string S) {
		int num = 0;
		for (int i = 0; i < J.size(); i++) {
			for (int j = 0; j < S.size(); j++) {
				if (J[i] == S[j]) num++;
			}
		}
		return num;
	}
};
```
## 938. Range Sum of BST
```C++
class Solution {
public:
	int rangeSumBST(TreeNode* root, int L, int R) {
		if (root == nullptr) return 0;
		int sum = 0;
		if (root->val > R) { sum += rangeSumBST(root->left, L, R); }
		if (root->val < L) { sum += rangeSumBST(root->right, L, R); }
		if (root->val >= L && root->val <= R) { sum += root->val + rangeSumBST(root->left, L, R) + rangeSumBST(root->right, L, R); }
		return sum;
	}
};
```

## 595. Big Countries
```SQL
# Write your MySQL query statement below
SELECT name, population, area
FROM World
WHERE area > 3000000 

UNION

SELECT name, population, area
FROM World
WHERE population > 25000000
```
## 804. Unique Morse Code Words
```C++
class Solution {
public:
	int uniqueMorseRepresentations(vector<string>& words) {
		if (words.size() == 0) return 0;
		vector<string> table = { ".-","-...","-.-.","-..",".","..-.",
			"--.","....","..",".---","-.-",".-..","--","-.","---",".--.",
			"--.-",".-.","...","-","..-","...-",".--","-..-","-.--","--.." };
		for (int j = 0; j < words.size(); j++) {
			string s = "";
			for (int i = 0; i < words[j].size(); i++) {
				s += table[words[j][i] - 'a'];
			}
			words[j] = s;
		}
		sort(words.begin(), words.end());
		int res = 1;
		for (int i = 0; i < words.size() - 1; i++) {
			if (words[i] != words[i + 1]) res++;
		}
		return res;
	}
};
```
## 961. N-Repeated Element in Size 2N Array
```C++
class Solution {
public:
	int repeatedNTimes(vector<int>& A) {
		int i = 0, j = 0, n = A.size();
		while (i == j || A[i] != A[j])
			i = rand() % n, j = rand() % n;
		return A[i];
	}
};

```
## 657. Robot Return to Origin
```C++
class Solution {
public:
	bool judgeCircle(string moves) {
		if (count(moves.begin(), moves.end(), 'L') == count(moves.begin(), moves.end(), 'R') && count(moves.begin(), moves.end(), 'U') == count(moves.begin(), moves.end(), 'D'))
			return true;
		else
			return false;
	}
};
```
## 1078. Occurrences After Bigram
```C++
class Solution {
public:
	vector<string> findOcurrences(string text, string first, string second) {
		vector<string> tmp,res;
		string str = "";
		for (int i = 0; i < text.length(); i++) {			
			if (text[i] != ' ') str += text[i];
			else {
				tmp.push_back(str);
				str = "";
			}
		}
		tmp.push_back(str);
		for (int i = 0; i < tmp.size() - 2; i++) {
			if (tmp[i] == first && tmp[i + 1] == second) res.push_back(tmp[i + 2]);
		}
		return res;
	}
};
```
## 852. Peak Index in a Mountain Array
```C++
class Solution {
public:
	int peakIndexInMountainArray(vector<int>& A) {
		int i = 0;
		for (; i < A.size() - 1; i++) {
			if (A[i] > A[i + 1]) break;
		}
		return i;
	}
};
```
## 933. Number of Recent Calls
```C++
class RecentCounter {
public:
	queue<int> q;
	RecentCounter() {

	}

	int ping(int t) {
		q.push(t);
		while (q.front() < t - 3000)
			q.pop();
		return q.size();
	}
};
```
## 944. Delete Columns to Make Sorted
```C++
class Solution {
public:
	int minDeletionSize(vector<string>& A) {
		if (A.size() == 0) return 0;
		vector<char> inc(A[0].size(), 'a');
		vector<bool> flag(A[0].size(), true);
		for (auto s : A) {
			for (int i = 0; i < s.size(); i++) {
				if (s[i] >= inc[i]) inc[i] = s[i];
				else flag[i] = false;
			}
		}
		return count(flag.begin(),flag.end(),false);
	}
};
```
## 627. Swap Salary
```SQL
# Write your MySQL query statement below
update salary set sex= CHAR(ASCII('f') + ASCII('m') - ASCII(sex));
```
## 700. Search in a Binary Search Tree
```C++
class Solution {
public:
	TreeNode* searchBST(TreeNode* root, int val) {
		if (root == nullptr) return nullptr;
		if (root->val == val) return root;
		else if (root->val > val) return searchBST(root->left, val);
		else return searchBST(root->right, val);
	}
};

```
## 590. N-ary Tree Postorder Traversal
```C++
class Solution {
public:
	vector<int> postorder(Node* root) {	
		if (root == nullptr) return {};
		vector<int> res;
		stack<Node*> tmp;
		tmp.push(root);
		while (!tmp.empty()) {
			Node* node = tmp.top();
			tmp.pop();
			for (int i = 0; i < node->children.size(); i++) tmp.push(node->children[i]);
			res.push_back(node->val);
		}
		reverse(res.begin(), res.end());
		return res;
	}
};
```
## 589. N-ary Tree Preorder Traversal
```C++
class Solution {
public:
	vector<int> preorder(Node* root) {
		if (root == nullptr) return {};
		vector<int> res;
		dfs(root, res);
		return res;
	}

	void dfs(Node* root, vector<int>& res) {
		if (root == nullptr) return;
		res.push_back(root->val);
		for (auto i : root->children)
			dfs(i, res);
	}
};
```
## 965. Univalued Binary Tree
```C++
class Solution {
public:
	bool isUnivalTree(TreeNode* root) {
		if (root == nullptr) return true;
		int tmp = root->val;
		if (root->right != nullptr && root->left != nullptr) 
			return (tmp == root->left->val) && (tmp == root->right->val) && isUnivalTree(root->left) && isUnivalTree(root->right);
		else if (root->right != nullptr && root->left == nullptr)
			return (tmp == root->right->val) && isUnivalTree(root->right);
		else if (root->right == nullptr && root->left != nullptr)
			return (tmp == root->left->val) && isUnivalTree(root->left);
		else return true;
        return false;		
	}
};
```
## 559. Maximum Depth of N-ary Tree
```C++
class Solution {
public:
	int maxDepth(Node* root) {
		if (root == nullptr) return 0;
		int res = 1;
		for (auto i : root->children)
			res = max(res, maxDepth(i) + 1);
		return res;
	}
};

```
## 788. Rotated Digits
```C++
class Solution {
public:
	int rotatedDigits(int N) {	
		int res = 0;
		for (int i = 0; i <= N; i++) {
			string s = to_string(i);
			int j = 0;
			string str = s;
			for (; j < s.size(); j++) {
				if(s[j] == '3' || s[j] == '4' || s[j] == '7') break;
				if (s[j] == '2') s[j] = '5';
				else if (s[j] == '5') s[j] = '2';
				else if (s[j] == '6') s[j] = '9';
				else if (s[j] == '9') s[j] = '6';
				else {}
			}
			if (j == s.size() && str != s) res++;
		}
		return res;
	}
};
```