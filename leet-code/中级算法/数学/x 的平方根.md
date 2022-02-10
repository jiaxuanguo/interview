# [x 的平方根](https://leetcode-cn.com/leetbook/read/top-interview-questions-medium/xwrzwc/)

### algorithm:
- 如果需要小数，可以用newton-raphson
- 既然不需要小数，用二分查找找到i，使i*i<=x<(i+1)*(i+1)
- 根据题目要求，二分查找的上限是2^16

### code:
```javascript
/**
 * @param {number} x
 * @return {number}
 */
var mySqrt = function(x) {
    let i = 0
    let j = Math.pow(2, 16)
    while (i <= j) {
        const mid = Math.floor((i + j) / 2)
        const next = mid + 1
        if (mid * mid <= x && next * next > x) {
            return mid
        } else if (mid * mid > x) {
            j = mid - 1
        } else {
            i = next
        }
    }
    throw new Error("shouldn't reach here")
}
```
