# Remove Duplicates from Sorted Array

[LeetCode Problem Array](https://leetcode.com/explore/interview/card/top-interview-questions-easy/92/array/727/)

## Описание задачи
A non-decreasing array of `nums' is given. Remove duplicates so that each unique element occurs only once. 
The relative order of the elements must be preserved. Return the number of unique elements `k`.

Modify the `nums' array so that the first `k` elements contain unique elements.

## Перевод для тех, кто плохо знает английский:
Дан отсортированный по неубыванию массив `nums`. Удалите дубликаты так, чтобы каждый уникальный элемент встречался только один раз. 
Относительный порядок элементов должен сохраниться. Верните количество уникальных элементов `k`.

Измените массив `nums` так, чтобы первые `k` элементов содержали уникальные элементы.

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

## Сложность
- Временная: O(n) — один проход по массиву  
- Пространственная: O(1) — изменение массива выполняется in-place  

---

*Задача решена с использованием двух указателей и модификации входного массива без дополнительных структур данных.*





