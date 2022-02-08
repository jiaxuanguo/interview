# [前 K 个高频元素](https://leetcode-cn.com/leetbook/read/top-interview-questions-medium/xvzpxi/)

### algorithm:
1. 遍历数组，使用HashMap记录每个数出现的次数
2. 获取map的entities，然后根据value排序
3. 返回前面的k个key

### code:
```javascript
/**
 * @param {number[]} nums
 * @param {number} k
 * @return {number[]}
 */
var topKFrequent = function(nums, k) {
    const counts = new Map()
    nums.forEach(num => counts.set(num, (counts.get(num) ?? 0) + 1))
    return Array
    .from(counts.entries())
    .sort((a, b) => b[1] - a[1])
    .map(([key, value]) => key)
    .slice(0, k)
}
```
