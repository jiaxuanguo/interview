# [Excel表列序号](https://leetcode-cn.com/leetbook/read/top-interview-questions-medium/xweb76/)

### algorithm:
本质上是转换不含0的26进制

### code:
```javascript
/**
 * @param {string} columnTitle
 * @return {number}
 */
var titleToNumber = function(columnTitle) {
    const charToNum = char => char.charCodeAt(0) - 'A'.charCodeAt(0) + 1
    return columnTitle
        .split('')
        .reverse()
        .map((char, power) => charToNum(char) * Math.pow(26, power))
        .reduce((acc, cur) => acc + cur)
}
```
