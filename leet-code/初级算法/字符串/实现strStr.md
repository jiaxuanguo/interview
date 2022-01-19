# [实现 strStr](https://leetcode-cn.com/leetbook/read/top-interview-questions-easy/xnr003/)

### algorithm:
1. 暴力法，双指针
2. boyer moore - bad character/good suffix
3. rabin karp - rolling hash
4. knuth morris pratt - dfa

### corner case:
- needle长度为0时返回0

### code:
```javascript
/**
 * @param {string} haystack
 * @param {string} needle
 * @return {number}
 */
var strStr = function(haystack, needle) {
    if (!needle) {
        return 0
    }
    for (let i = 0; i <= haystack.length - needle.length; i++) {
        for (let j = 0; j < needle.length; j++) {
            if (haystack[i + j] === needle[j]) {
                if (j === needle.length - 1) {
                    return i
                }
            } else {
                break
            }
        }
    }
    return -1
};
```
