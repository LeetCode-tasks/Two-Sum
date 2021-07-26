# Two Sum

Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

### Example:

**_Input:_** `nums = [2,7,11,15], target = 9`

**_Output:_** `[0,1]`

Because `nums[0] + nums[1] == 9`, we return `[0, 1]`.

### Constraints:

`2 <= nums.length <= 10^4`

`-10^9 <= nums[i] <= 10^9`

`-10^9 <= target <= 10^9`

**Only one valid answer exists.**
 
## Solution in JavaScript:

```
var twoSum = function(nums, target) {
    let targetFirstIndex, targetLastIndex;
    
    for (let i = 0; i < nums.length; i++) {
        for (let j = i + 1; j < nums.length; j++) {
            if (nums[i] + nums[j] === target) {
                targetFirstIndex = i;
                targetLastIndex = j;
                break;
            } 
        }
    }
    
    return [targetFirstIndex, targetLastIndex];
};
```
