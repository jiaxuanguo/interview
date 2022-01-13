# [两个数组的交集 II](https://leetcode-cn.com/leetbook/read/top-interview-questions-easy/x2y0c2/)

### algorithm:
1. 常规算法，利用两个HashMap；空间复杂度O(n)，时间复杂度O(n)
   1. 用两个HashMap m1和m2分别记录每个数组中的数字和出现的次数
   2. 数字i在交集数组中的次数应为min(m1.get(i), m2.get(i))
   3. 对m1中的每一个key，按ii得到其次数并加入交集数组
2. 两个数组长度相差悬殊时，只用HashMap记录短数组的数字和次数。每次将数字加入交集数组后将HashMap中该数字的次数-1
3. 数组已排序时可用双指针；空间复杂度O(1)，时间复杂度O(n)

### code:
```javascript
const LENGTH_RATIO_THRESHOLD = 100
/**
 * @param {number[]} nums1
 * @param {number[]} nums2
 * @return {number[]}
 */
var intersect = function(nums1, nums2) {
    if (nums1.length / nums2.length > LENGTH_RATIO_THRESHOLD) {
        return umbalanced(nums1, nums2)
    } else if (nums2.length / nums1.length > LENGTH_RATIO_THRESHOLD) {
        return umbalanced(nums2, nums1)
    } else {
        return simple(nums1, nums2)
    }
};

const simple = (nums1, nums2) => {
    const m1 = new Map()
    nums1.forEach(num => {
        const count = m1.get(num) ?? 0
        m1.set(num, count + 1)
    })
    const m2 = new Map()
    nums2.forEach(num => {
        const count = m2.get(num) ?? 0
        m2.set(num, count + 1)
    })
    return Array.from(m1.entries())
    .map(([num, count]) => [num, Math.min(count, m2.get(num) ?? 0)])
    .filter(([, count]) => count > 0)
    .map(([num, count]) => Array(count).fill(num))
    .flat()
}

const umbalanced = (long, short) => {
    const m = new Map()
    short.forEach(num => {
        const count = m.get(num) ?? 0
        m.set(num, count + 1)
    })
    const intersect = []
    long.forEach(num => {
        const count = m.get(num)
        if (count) {
            intersect.push(num)
            m.set(num, count - 1)
        }
    })
    return intersect
}
```
