# [Pow(x, n)](https://leetcode-cn.com/leetbook/read/top-interview-questions-medium/xwo102/)

### algorithm:
- 如果n<0，将n变为-n，x变为1/x
- 从1开始，乘n次x；时间复杂度O(n)
- `pow(x,n)=pow(pow(x,n/2), 2)*pow(x,n%2)`；时间复杂度O(logn)

### code:
```javascript
/**
 * @param {number} x
 * @param {number} n
 * @return {number}
 */
var myPow = function(x, n) {
    if (n < 0) {
        n = -n
        x = 1 / x
    }
    if (n === 0) {
        return 1
    } else if (n === 1) {
        return x
    } else if (n === 2) {
        return x * x
    } else {
        return myPow(myPow(x, Math.floor(n / 2)), 2) * myPow(x, n % 2)
    }
}
```
