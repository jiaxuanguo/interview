# [删除链表的倒数第N个节点](https://leetcode-cn.com/leetbook/read/top-interview-questions-easy/xn2925/)

### algorithm:
1. 使用前后双指针
2. 从head开始，前指针先移动n个节点
3. 两个指针按相同速度一起移动
4. 当前指针指向最后一个节点时，后指针正好指向倒数n+1个节点
5. 利用后指针删除第n个节点

### corner case:
如果完成第2步后前指针已指向null，说明需删除第一个节点，直接返回head.next即可
也可以在head前添加一个节点作为新head来避免此corner case

### code: 
```javascript
/**
 * Definition for singly-linked list.
 * function ListNode(val, next) {
 *     this.val = (val===undefined ? 0 : val)
 *     this.next = (next===undefined ? null : next)
 * }
 */
/**
 * @param {ListNode} head
 * @param {number} n
 * @return {ListNode}
 */
var removeNthFromEnd = function(head, n) {
    let steps = n
    let i = head
    let j = head
    while (steps) {
        j = j.next
        steps--
    }
    if (j === null) {
        return head.next
    }
    while (j.next) {
        i = i.next
        j = j.next
    }
    i.next = i.next.next
    return head
}
```
