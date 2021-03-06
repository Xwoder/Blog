# [LeetCode] 151. Reverse Words in a String

[TOC]

## 链接

[151. Reverse Words in a String](https://leetcode.com/problems/reverse-words-in-a-string/)

## 题目

Given an input string, reverse the string word by word.

**Example 1:**

```text
Input: "the sky is blue"
Output: "blue is sky the"
```

**Example 2:**

```text
Input: "  hello world!  "
Output: "world! hello"
Explanation: Your reversed string should not contain leading or trailing spaces.
```

**Example 3:**

```text
Input: "a good   example"
Output: "example good a"
Explanation: You need to reduce multiple spaces between two words to a single space in the reversed string.
```

**Note:**

* A word is defined as a sequence of non-space characters.
* Input string may contain leading or trailing spaces. However, your reversed string should not contain leading or trailing spaces.
* You need to reduce multiple spaces between two words to a single space in the reversed string.

## 代码

> `Swift` 语言

```Swift
class Solution {
    func reverseWords(_ s: String) -> String {
        return s.split(separator: " ")
            .reversed()
            .joined(separator: " ")
    }
}
```

