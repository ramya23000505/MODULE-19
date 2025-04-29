# EX 1B Merge Sort
## DATE: 22-03-2025
## AIM:
To write a python program to sort the first half of the list using merge sort.

## Algorithm
1. Start

2. Read the number of elements n.

3. Read the array of n integers into inp_arr.

4. Call the function merge_sort(inp_arr) to sort the array.

5. Inside merge_sort(arr):

Step 1: If the length of arr is more than 1:

Step 2: Find the middle index of the array.

Step 3: Split the array into two halves: left_arr and right_arr.

Step 4: Recursively call merge_sort(left_arr) and merge_sort(right_arr).

Step 5: Initialize pointers p, q, and r to 0.

Step 6: While both left_arr and right_arr have unprocessed elements:

Compare left_arr[p] and right_arr[q]

Place the smaller value into arr[r] and move the pointers accordingly.

Step 7: Copy any remaining elements from left_arr (if any).

Step 8: Copy any remaining elements from right_arr (if any).

6. After the recursive sorting is complete, print the sorted array.

7. End 

## Program:
```
/*
Program to implement Merge Sort
Developed by: RAMYA R
Register Number: 212223230169  
*/

def merge_sort(inp_arr):
    size = len(inp_arr)
    #divide
    if size > 1:
        middle = size //2
        left_arr = inp_arr[:middle]
        right_arr = inp_arr[middle:]
        merge_sort(left_arr)
        merge_sort(right_arr)
        p=0 # first number of first table
        q=0 # first number of second table
        r=0 # combined table
        
        # combine
        left_size = len(left_arr)
        right_size = len(right_arr)
        # self table
        while p <left_size and q < right_size:
            if left_arr[p] < right_arr[q]:
                inp_arr[r] = left_arr[p]
                p+=1
            else:
                inp_arr[r] = right_arr[q]
                q+=1
            r+=1
        # check size    
        while p < left_size:
            inp_arr[r] = left_arr[p]
            p+=1
            r+=1
        while q < right_size:
            inp_arr[r] = right_arr[q]
            q+=1
            r+=1

inp_arr = []
n=int(input())
for i in range(n):
    inp_arr.append(int(input()))
    
print("Input Array:\n")
print(inp_arr)
merge_sort(inp_arr)

print("Sorted Array:\n")
print(inp_arr)

            
                
```

## Output:

![image](https://github.com/user-attachments/assets/faf75b16-5b8a-4676-bd20-22dd021d2059)


## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
