# Technical coding interviews - Ideas

Some problems could not be categrized into "data structure" or "algorithm".

We should collect experiences about the key ideas of these "non-standard" problems. That is why this folder exists.

### Large numbers as binary codes

For large integers, some problems would be directly related to their binary codes of them. And somtimes we would initiatively use binary codes to solve particular problems.

**For Leetcode-600**, we consider the "buiding process" of binary codes of intergers:
```python
0      0
1      1
2     10
3     11
4    100   1 + "00"
5    101   1 + "01"
6    110   1 + "10"
7    111   1 + "11"
8   1000     1 + "000"   
9   1001     1 + "001"
10  1010     1 + "010"
11  1011     1 + "011"
12  1100     1 + "100"
13  1101     1 + "101"
14  1110     1 + "110"
15  1111     1 + "111"
```
It is clear that the binary codes of [8, 15] are the concatenation the the leading "1" and binary codes of [0, 7]. Therefore we can build a DP-like solving process.

(Note) For Leetcode-600, the non-DP Fibonacci solution is the fastest. Say the length of the binary code is k, then f(k) = f(k - 1) + f(k - 2):
- f(k - 2): leading with "10"
- f(k - 1): leading with "11"

But the Fibonacci may be another issue.



##### Related problems:
- [[Leetcode-260] Single Number III](https://leetcode.com/problems/single-number-iii/description/)
- [[Leetcode-600] Non-negative Integers without Consecutive Ones](https://leetcode.com/problems/non-negative-integers-without-consecutive-ones/description/)
