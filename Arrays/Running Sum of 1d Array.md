# 1480 – Running Sum of 1d Array

## Problem:
Given an array nums. We define a running sum of an array as runningSum[i] = sum(nums[0]…nums[i]).
Return the running sum of nums.

## Example 1:
Input: nums = [1,2,3,4]
Output: [1,3,6,10]
Explanation: Running sum is obtained as follows: [1, 1+2, 1+2+3, 1+2+3+4].

## Approach:
1. Reframe the given array
2. Traverse the nums using for loop

## Java Solution:
```java
class Solution {
    public int[] runningSum(int[] nums) {
        int n=nums.length;
        for(int i=1;i<n;i++){
            nums[i]=nums[i]+nums[i-1];
        }
        return nums;
    }
}
```
