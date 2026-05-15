# leetcode-DSA-solutions

---
# Arrays - Easy
## [1480 - RunningSum.java](https://leetcode.com/problems/running-sum-of-1d-array/)
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

## [Second Largest](https://www.geeksforgeeks.org/problems/second-largest3735/)
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
## [1-Two Sum](https://leetcode.com/problems/two-sum/)
``` DSA
class Solution {
    public int[] twoSum(int[] nums, int target) {
        int sum;
        for(int i =0; i<nums.length;i++){
          for(int j = i+1; j<nums.length;j++){
            sum = nums[i]+nums[j];
            if(sum == target){
                return new int[]{i,j};
                
            
    }
}
        }
        return new int[]{};
    }
    
}
        
```
## [35-Search Insert Position](https://leetcode.com/problems/search-insert-position/)
```DSA
class Solution {
    public int searchInsert(int[] nums, int target) {
        for(int i=0;i<nums.length;i++){
            if(nums[i] >= target){
                return i;
            }
        }
        return nums.length;

    }
}
```
## [283 - Move Zeroes](https://leetcode.com/problems/move-zeroes/description/)
```DSA
class Solution {
    public void moveZeroes(int[] nums) {
        int j =0;
        for(int i=0;i<nums.length;i++){
            if(nums[i]!=0){
                int temp = nums[i];
                nums[i] = nums[j];
                nums[j] = temp;
                j++;
            }
        }
    }
}
```
## [2529 - Maximum Count Of Positive Integer and Negative Integer](https://leetcode.com/problems/maximum-count-of-positive-integer-and-negative-integer/description/)
```DSA
class Solution {
    public int maximumCount(int[] nums) {
        int positive = 0;
        int negative = 0;
        for(int i=0; i<nums.length;i++){
            if(nums[i]>0){
                positive++;
            }
            if(nums[i]<0){
                negative++;
            }
        }
            int max_count = Math.max(positive,negative);

            return max_count;
        }
     
    }
```


# Arrays - Medium
## [53-Maximum SubArray](https://leetcode.com/problems/maximum-subarray/)
```DSA
class Solution {               
    public int maxSubArray(int[] a) {
        int max_sum = a[0]; 
        int sum = a[0];
        for(int i=1;i<a.length;i++){
            if(sum<0){
                sum = a[i];
            }
            else{
            sum = sum+a[i];
            }
            max_sum = Math.max(max_sum,sum);
            }                                                                                                                                                         
            return max_sum;
        }
} 
```








