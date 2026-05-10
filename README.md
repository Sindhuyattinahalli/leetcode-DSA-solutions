# leetcode-DSA-solutions

---
# Arrays - easy
## [1480 - Arrays/Easy/RunningSum.java](https://leetcode.com/problems/running-sum-of-1d-array/)
``` DSA
class Solution {
    public int[] runningSum(int[] nums) {
        int b[] = new int[nums.length];
        int sum = 0;
        for(int i=0;i<nums.length;i++){
            sum = sum + nums[i];
             b[i] = sum ;
        }
        return b ; 
        
    }
}
```
