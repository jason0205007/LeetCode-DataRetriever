# [5] Longest Palindromic Substring (Medium)

[![String_badge](https://img.shields.io/badge/topic-String-green.svg)](https://leetcode.com/problems/longest-palindromic-substring/)  [![Dynamic%20Programming_badge](https://img.shields.io/badge/topic-Dynamic%20Programming-green.svg)](https://leetcode.com/problems/longest-palindromic-substring/) 

:+1: 7608 &nbsp; &nbsp; :thumbsdown: 562

---

## My Submission

- Language: python3
- Runtime: 964 ms
- Completed time: 2020-08-02 17:50:16

```python3
class Solution:
    def findPalindrome(self, s: str, i: int, j: int):
        while i >= 0 and j < len(s) and s[i] == s[j]:
            i -= 1
            j += 1
        return j - i - 1
    
    def longestPalindrome(self, s: str) -> str:
        ret = ""
        i = 0
        j = 0
        p_len = 0
        for c, v in enumerate(s):
            odd = self.findPalindrome(s, c, c)
            even = self.findPalindrome(s, c, c + 1)
            currentMax = max(odd, even)
            if currentMax > p_len:
                p_len = currentMax
                print(p_len, c)
                i = c - (p_len - 1) // 2
                j = c + p_len // 2
            
        return s[i:j+1]
```

## Content
<p>Given a string <strong>s</strong>, find the longest palindromic substring in <strong>s</strong>. You may assume that the maximum length of <strong>s</strong> is 1000.</p>

<p><strong>Example 1:</strong></p>

<pre>
<strong>Input:</strong> &quot;babad&quot;
<strong>Output:</strong> &quot;bab&quot;
<strong>Note:</strong> &quot;aba&quot; is also a valid answer.
</pre>

<p><strong>Example 2:</strong></p>

<pre>
<strong>Input:</strong> &quot;cbbd&quot;
<strong>Output:</strong> &quot;bb&quot;
</pre>


## Related Problems
[Shortest Palindrome](https://leetcode.com/problems/shortest-palindrome/) (Hard) <br>
[Palindrome Permutation](https://leetcode.com/problems/palindrome-permutation/) (Easy) <br>
[Palindrome Pairs](https://leetcode.com/problems/palindrome-pairs/) (Hard) <br>
[Longest Palindromic Subsequence](https://leetcode.com/problems/longest-palindromic-subsequence/) (Medium) <br>
[Palindromic Substrings](https://leetcode.com/problems/palindromic-substrings/) (Medium) <br>

## What a(n) Medium problem!
Among **3388121** total submissions, **999797** are accepted, with an acceptance rate of **29.5%**. <br>

- Likes: 7608
- Dislikes: 562

