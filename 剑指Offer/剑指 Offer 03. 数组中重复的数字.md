## Problem

> [剑指 Offer 03. 数组中重复的数字](https://leetcode.cn/problems/shu-zu-zhong-zhong-fu-de-shu-zi-lcof)



## Code
### First Solution

**Complexity**

- time complexity: $O(n)$
- space complexity: $O(1)$

**Java**

```java
class Solution {
    public int findRepeatNumber(int[] nums) {
        for(int i = 0; i < nums.length; ){
            if(i == nums[i]){
                i++;
                continue;
            }
            // means there is a repeated number
            if (nums[i] == nums[nums[i]]) {
                return nums[i];
            }
          	// swap num to the correct position 
            int tmp = nums[i];
            nums[i] = nums[tmp];
            nums[tmp] = tmp;
        }
        return -1;
    }
}

```