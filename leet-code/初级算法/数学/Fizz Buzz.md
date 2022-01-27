# [Fizz Buzz](https://leetcode-cn.com/leetbook/read/top-interview-questions-easy/xngt85/)

### algorithm:
按题目描述循环添加元素即可

### code:
```javascript
/**
 * @param {number} n
 * @return {string[]}
 */
var fizzBuzz = function(n) {
    const result = []
    for (let i = 1; i <= n; i++) {
        let str
        if (i % 15 === 0) {
            str = 'FizzBuzz'
        } else if (i % 5 === 0) {
            str = 'Buzz'
        } else if (i % 3 === 0) {
            str = 'Fizz'
        } else {
            str = '' + i
        }
        result.push(str)
    }
    return result
}
```
