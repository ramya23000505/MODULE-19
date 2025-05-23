# EX 1C Quick Sort
## DATE: 04-03-2025
## AIM:
To write a python program to implement quick sort using tha last element as pivot on the list of float values.

## Algorithm
1. Start the program.

2. Read the number of elements n and store the input values in a list called array.

3. Determine the midpoint of the list using mid = n // 2.

4. Apply Quick Sort only on the second half of the list: from index mid to n-1.

5. Use recursion to implement Quick Sort:
   Select a pivot element and partition the array such that smaller elements go to the left and larger ones to the right.

6. Update the original list with the sorted second half while keeping the first half unchanged.

7. Display the final list and end the program.  

## Program:
```
/*
Program to implement implement quick sort using the last element as pivot on the list of float values.
Developed by: RAMYA R
Register Number:  212223230169
*/
def pivot(array, start, end):
    pivot = array[start]
    low = start + 1
    high = end
 
 
    while True:
        while low <= high and array[high] >= pivot:
            high = high - 1
        while low <= high and array[low] <= pivot:
            low = low + 1
        if low <= high:
            array[low], array[high] = array[high], array[low]
          
        else:
            break
    array[start], array[high] = array[high], array[start]
    return high
 
 
def quick_sort(array, start, end):
    if start >= end:
        return
    p = pivot(array, start, end)
    quick_sort(array, p+1, end)

array = []
n=int(input())
for i in range(n):
    array.append(int(input()))
quick_sort(array, 0, len(array) - 1)
print(array)
```

## Output:
![image](https://github.com/user-attachments/assets/404afd0b-bf65-4a3f-a906-9c3569c66952)



## Result:
The program successfully sorts the second half of the input list using Quick Sort with recursion, while leaving the first half unchanged.
