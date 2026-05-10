# leetcode-DSA-solutions

---
# Arrays - Easy
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
---

## [# Arrays - Easy /Second Largest](https://www.geeksforgeeks.org/problems/second-largest3735/)
```DSA
class Solution {
    public int getSecondLargest(int[] arr) {
        int largest = Integer.MIN_VALUE;
        int SLargest = Integer.MIN_VALUE;
        for(int i=0; i<arr.length;i++){
            if(arr[i] > largest){
                SLargest = largest;
                largest = arr[i]; 
            }
            else if(arr[i] > SLargest && arr[i] != largest){
                SLargest = arr[i];
                } 
        }
        return (SLargest == Integer.MIN_VALUE) ? -1 : SLargest;
    }
    }
```





