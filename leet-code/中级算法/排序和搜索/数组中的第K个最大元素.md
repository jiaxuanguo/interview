# [数组中的第K个最大元素](https://leetcode-cn.com/leetbook/read/top-interview-questions-medium/xvsehe/)

### algorithm:
quick select
- 部分快排
- 根据k判断目标元素在哪个子数组
- 后续只递归处理存在目标元素的子数组

### code:
```javascript
/**
 * @param {number[]} nums
 * @param {number} k
 * @return {number}
 */
var findKthLargest = function(nums, k) {
    const partition = (i, j) => {
        const pivot = nums[j]
        let m = i - 1
        for (let n = i; n < j; n++) {
            if (nums[n] < pivot) {
                m++
                const temp = nums[m]
                nums[m] = nums[n]
                nums[n] = temp
            }
        }
        const index = m + 1
        nums[j] = nums[index]
        nums[index] = pivot
        return index
    }
    const quickSelect= (i, j, k) => {
        const m = partition(i, j)
        if (m === k) {
            return nums[m]
        } else if (m < k) {
            return quickSelect(m + 1, j, k)
        } else {
            return quickSelect(i, m - 1, k)
        }
    }
    return quickSelect(0, nums.length - 1, nums.length - k)
}
```
