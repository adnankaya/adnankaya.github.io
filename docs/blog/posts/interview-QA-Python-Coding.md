---
date:
  created: 2024-09-26
  updated: 2024-09-26
readtime: 10
pin: false
links:
  - Homepage: index.md#project-layout
  - Blog index: blog/index.md
  - External links:
    - Web Page: https://adnankaya.github.io
categories:
  - Python
  - Coding
  - Interview
tags:
  - python
  - interview
  - coding
  - techincal
authors:
  - adnankaya
slug: interview-questions-answers-python-coding
---

# Python Coding Interview Questions and Answers

Let's prepare python coding interview!

<!-- more -->
## 1. Even Numbers
- Write a Python function that takes a list of integers and returns a new list containing only the even numbers from the original list.

=== "Question"
  
    ```python
    def filter_even_numbers(numbers: list[int]) -> list[int]:
    # Your code here
    ```

=== "Solution 1"

    ```python
    def filter_even_numbers(numbers: list[int]) -> list[int]:
      even_numbers: list[int] = []
      for num in numbers:
          if num % 2 == 0:
              even_numbers.append(num)
      return even_numbers
    """
    Time Complexity:
    The function iterates over each element in the numbers list once, 
    checking if it is even, which takes O(1) time. 
    Therefore, the time complexity is O(n), 
    where n is the number of elements in the list.

    Space Complexity:
    The space complexity is O(n), where n is the number of even numbers in the list. 
    This is because you are creating a new list even_numbers to store the result.
    """
    ```
    
=== "Solution 2"

    ```python
    def filter_even_numbers(numbers: list[int]) -> list[int]:
      return [num for num in numbers if num % 2 == 0]
    """
    This version is shorter, cleaner, and equally efficient.
    """
    ```

## 2. Anagram String Comparison
- Write a Python function that takes two strings and returns True if one string is an anagram of the other (i.e., they contain the same characters in the same frequencies. HEART & EARTH , SILENT & LISTEN, SADDER & DREADS are anagram strings), and False otherwise.

=== "Question"

    ``` python
    def are_anagrams(s1: str, s2: str) -> bool:
    # Your code here
    ```

=== "Solution 1"

    ```python
    def are_anagrams(s1: str, s2: str) -> bool:
      if not (len(s1) == len(s2)):
          return False

      # count s1 character frequency
      s1freq = {}
      for i in s1:
          counter = 0
          for j in s1:
              if i == j:
                  counter += 1
          s1freq[i] = counter
      # count s2 character frequency
      s2freq = {}
      for i in s2:
          counter = 0
          for j in s2:
              if i == j:
                  counter += 1
          s2freq[i] = counter

      # compare for anagram
      for k, v in s1freq.items():
          if not (k in s2freq and v == s2freq[k]):
              return False
      return True
    """
    Time Complexity:
    Your code has a nested loop to calculate the frequency of characters for both strings. 
    For each character in the string (O(n)), you are checking the entire string again (O(n)), 
    making the time complexity O(n^2) where n is the length of the string.

    Space Complexity:
    You are using two dictionaries to store character frequencies, 
    so the space complexity is O(n), 
    where n is the number of unique characters in the string.
    """
    ```
=== "Solution 2"

    ```python
    def are_anagrams(s1: str, s2: str) -> bool:
      if not (len(s1) == len(s2)):
          return False
      # count s1 character frequency
      s1freq = {}
      for i in s1:
          s1freq[i] = s1freq.get(i, 0) + 1
      # count s2 character frequency
      s2freq = {}
      for i in s2:
          s2freq[i] = s2freq.get(i, 0) + 1
      # compare for anagram
      for k, v in s1freq.items():
          if not (k in s2freq and v == s2freq[k]):
              return False
      return True
    """
    Time Complexity:

    Counting the frequency of characters in both s1 and s2 takes 
    O(n), where n is the length of the strings.
    Comparing the frequency dictionaries also takes 
    O(n). Therefore, the overall time complexity is O(n), where 
    n is the length of the strings.
    Space Complexity:

    You are creating two dictionaries (s1freq and s2freq) to store character frequencies, 
    so the space complexity is O(k), where 
    k is the number of unique characters in the strings.
    """
    ```
=== "Solution 3"

    ```python
    def are_anagrams(s1: str, s2: str) -> bool:
      return sorted(s1) == sorted(s2)
    
    """
    Time Complexity: Sorting takes 
    O(nlogn), where n is the length of the strings.
    Space Complexity: 
    O(n) due to the space needed for the sorted strings.
    """
    ```

- TODOnextQuestion

=== "Question"

    ``` python
    
    ```

=== "Solution 1"

    ```python
    
    ```
=== "Solution 2"

    ```python
    
    ```