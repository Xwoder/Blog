# [LeetCode] 509. Fibonacci Number

[TOC]

## 链接

[509. Fibonacci Number](https://leetcode.com/problems/fibonacci-number/)

## 题目

> The Fibonacci numbers, commonly denoted `F(n)` form a sequence, called the Fibonacci sequence, such that each number is the sum of the two preceding ones, starting from `0` and `1`. That is,
> 
> ```
> F(0) = 0,   F(1) = 1
> F(N) = F(N - 1) + F(N - 2), for N > 1.
> ```
> 
> Given `N`, calculate `F(N)`.
>
> **Example 1:**
>
> ```
> Input: 2
> Output: 1
> Explanation: F(2) = F(1) + F(0) = 1 + 0 = 1.
> ```
> 
> **Example 2:**
>
> ```
> Input: 3
> Output: 2
> Explanation: F(3) = F(2) + F(1) = 1 + 1 = 2.
> ```
> 
> **Example 3:**
>
> ```
> Input: 4
> Output: 3
> Explanation: F(4) = F(3) + F(2) = 2 + 1 = 3.
> ```
>
> **Note:**
>
> 0 ≤ `N` ≤ 30.

## 代码

### 解法1

```Java
class Solution {
    public int fib(int N) {

        if (N < 2) {
            return N;
        }

        int first = 0;
        int second = 1;

        while (N >= 2) {
            int temp = second + first;
            first = second;
            second = temp;
            --N;
        }

        return second;
    }
}
```

### 解法2

```Java
class Solution {
    public int fib(int N) {

        int[] array = {
                0,
                1,
                1,
                2,
                3,
                5,
                8,
                13,
                21,
                34,
                55,
                89,
                144,
                233,
                377,
                610,
                987,
                1597,
                2584,
                4181,
                6765,
                10946,
                17711,
                28657,
                46368,
                75025,
                121393,
                196418,
                317811,
                514229,
                832040
        };

        return array[N];
    }
}
```

