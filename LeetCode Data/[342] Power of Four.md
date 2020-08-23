# [342] Power of Four (Easy)

[![Bit Manipulation_badge](https://img.shields.io/badge/topic-Bit Manipulation-green.svg)](https://leetcode.com/problems/power-of-four/) 

[Magic Portal](https://leetcode.com/problems/power-of-four/)

## My Submission

- Runtime: 4 ms
- Completed time: 2020-08-04 13:42:32

```cpp
class Solution {
public:
    bool isPowerOfFour(int num) {
        int mask = 1;
        while (mask < num && (mask != 0x40000000)) {
            cout << "mask" << mask << endl;
            mask = mask << 2;
        }

        cout << mask;
        return !(mask ^ num);
    }
};
```

## Content
<p>Given an integer (signed 32 bits), write a function to check whether it is a power of 4.</p>

<p><strong>Example 1:</strong></p>

<pre>
<strong>Input: </strong><span id="example-input-1-1">16</span>
<strong>Output: </strong><span id="example-output-1">true</span>
</pre>

<div>
<p><strong>Example 2:</strong></p>

<pre>
<strong>Input: </strong><span id="example-input-2-1">5</span>
<strong>Output: </strong><span id="example-output-2">false</span></pre>
</div>

<p><b>Follow up</b>: Could you solve it without loops/recursion?</p>

## Related Problems
[Power of Two](https://leetcode.com/problems/power-of-two/) (Easy) <br>
[Power of Three](https://leetcode.com/problems/power-of-three/) (Easy) <br>

## What a(n) Easy problem!
Among **487498** total submissions, **202105** are accepted, with an acceptance rate of 41.5%. <br>

- Likes: 679
- Dislikes: 235
