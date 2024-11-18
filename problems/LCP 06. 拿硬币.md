## [LCP 06. 拿硬币](https://leetcode.cn/problems/na-ying-bi/)

### First Solution

**Java**

```java
class Solution {
    public int minCount(int[] coins) {
        int count = 0;
        for(int coin : coins){
            if(coin % 2 == 0){
                count += coin / 2;
            } else {
                count += (coin / 2 + 1);
            }
        }
        return count;
    }
}

```

| time complexity | space complexity |
| --------------- | ---------------- |
| $O(n)$          | $O(1)$           |

