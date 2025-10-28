# leetcode238
## 📋 Problem Description

Given an integer array `nums`, return an array `answer` such that `answer[i]` is equal to the product of all the elements of `nums` except `nums[i]`.
The product of any prefix or suffix of `nums` is guaranteed to fit in a 32-bit integer.
You must write an algorithm that runs in **O(n)** time and without using the division operation.
### Example 1:
Input: nums = [1,2,3,4]
Output: [24,12,8,6]


### Example 2:
Input: nums = [-1,1,0,-3,3]
Output: [0,0,9,0,0]



##  Solution Approach

### Key Insight
For each element at index `i`, the product except self can be calculated as:
result[i] = (product of all elements to the left of i) × (product of all elements to the right of i)

### Algorithm
1. Left Pass: Calculate the running product of all elements to the left of each index
2. Right Pass: Calculate the running product of all elements to the right of each index and multiply with the left product

### Complexity Analysis
- Time Complexity: O(n) - Two passes through the array
- Space Complexity: O(1) - Only the output array is used (excluding input storage)



