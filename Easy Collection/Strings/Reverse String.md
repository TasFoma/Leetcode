# Reverse String

[LeetCode Problem #344 - Reverse String](https://leetcode.com/problems/reverse-string/)

## Описание задачи

Write a function that flips a string.  
The input string is represented as an array of `s` characters.  
You need to do this by changing the input array in-place using O(1) additional memory. 

## Примеры

**Пример 1:**  
Ввод: `s = ["h", "e", "l", "l", "o"]`  
Вывод: `["o", "l", "l", "e", "h"]`

**Пример 2:**  
Ввод: `s = ["H", "a", "n", "n", "a", "h"]`  
Вывод: `["h", "a", "n", "n", "a", "H"]` 

## Решение на C#
``` 
public class Solution {
  public void ReverseString(char[] s) {
   int left = 0;
   int right = s.Length - 1;
   while (left < right) {
        char temp = s[left];
        s[left] = s[right];
        s[right] = temp;

        left++;
        right--;
    }
 }
}
```

## Объяснение решения

Данное решение использует подход с двумя указателями:  
- Указатель `left` начинает с начала массива,  
- Указатель `right` — с конца массива.  
Мы меняем местами элементы, на которые указывают `left` и `right`, двигая указатели к центру, пока они не встретятся.  
Это позволяет перевернуть массив **на месте** без использования дополнительной памяти.
 
 

