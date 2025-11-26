# Remove Duplicates from Sorted Array

[LeetCode #26 - Remove Duplicates from Sorted Array](https://leetcode.com/explore/interview/card/top-interview-questions-easy/92/array/727/)

## Описание задачи
A non-decreasing array of `nums' is given. Remove duplicates so that each unique element occurs only once. 
The relative order of the elements must be preserved. Return the number of unique elements `k`.

Modify the `nums' array so that the first `k` elements contain unique elements. 

## Пример
**Ввод:** `nums = [1,1,2]`  
**Вывод:** `2, nums = [1,2,_]`  

## Решение на C#
```
public class Solution {
  public int RemoveDuplicates(int[] nums) {
    if (nums.Length == 0) return 0;
      int k = 0;
      for (int i = 1; i < nums.Length; i++) {
        if (nums[i] != nums[k]) {
          k++;
          nums[k] = nums[i];
        }
      }
    return k + 1;
  }
} 
```
 




