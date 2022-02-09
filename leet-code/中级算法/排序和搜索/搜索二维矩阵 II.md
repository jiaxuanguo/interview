# [搜索二维矩阵 II](https://leetcode-cn.com/leetbook/read/top-interview-questions-medium/xvc64r/)

### algorithm:
- 根据矩阵的特性，左下角的数是当前行最小的，也是当前列最大的
- 利用这点可以一次判断排除一行或一列：如果当前数比目标大，那么排除当前行，否则排除当前列

### code:
```javascript
/**
 * @param {number[][]} matrix
 * @param {number} target
 * @return {boolean}
 */
var searchMatrix = function(matrix, target) {
    let i = matrix.length - 1
    let j = 0
    while (i >= 0 && j < matrix[i].length) {
        const num = matrix[i][j]
        if (num === target) {
            return true
        } else if (num > target) {
            i--
        } else {
            j++
        }
    }
    return false
}
```
