# [二叉搜索树中第K小的元素](https://leetcode-cn.com/leetbook/read/top-interview-questions-medium/xvuyv3/)

### algorithm:
- 对二叉搜索树做中序遍历可以得到有序数组，返回第k个元素即可
- 或者在遍历过程中记录遍历的节点数i, 当`i===k`时记录当前节点的值。如此不需要完成遍历
- 如果二叉树会被频繁修改，可以在节点上记录该节点的子节点个数。查找时根据子节点数可以快速跳过部分子树

### code:
```javascript
/**
 * Definition for a binary tree node.
 * function TreeNode(val, left, right) {
 *     this.val = (val===undefined ? 0 : val)
 *     this.left = (left===undefined ? null : left)
 *     this.right = (right===undefined ? null : right)
 * }
 */
/**
 * @param {TreeNode} root
 * @param {number} k
 * @return {number}
 */
var kthSmallest = function(root, k) {
    let count = 0
    let val
    const traverse = node => {
        if (!node || val !== undefined) {
            return
        }
        traverse(node.left)
        count += 1
        if (count === k) {
            val = node.val
        }
        traverse(node.right)
    }
    traverse(root)
    return val
}
```
