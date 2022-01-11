[买卖股票的最佳时机 II](https://leetcode-cn.com/leetbook/read/top-interview-questions-easy/x2zsx1/)
###algorithm：
1. 贪心：local minimum买入，下一个local maximum卖出
2. 简化逻辑：每日都尝试卖出和买入。如果当日价格比当前买入价格低，则*重新买入*，否则*卖出并按当前价格买入*
###code:
```javascript
/**
 * @param {number[]} prices
 * @return {number}
 */
var maxProfit = function(prices) {
    let profit = 0
    let current = prices[0]
    for (let i = 1; i < prices.length; i++) {
        const price = prices[i]
        if (current > price) {
            current = price
        } else {
            profit += (price - current)
            current = price
        }
    }
    return profit
};
```
