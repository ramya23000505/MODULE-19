# EX 1B Merge Sort
## DATE: 22-03-2025
## AIM:
To write a Python program that implements the Merge Sort algorithm using recursion to sort an array of integers.

## Algorithm
1. Start the program.

2. Read the number of elements and store them in an array.

3. Check if the array has more than one element — if so, divide it into two halves.

4. Recursively apply merge sort to both halves of the array.

5. Merge the two sorted halves by comparing elements and placing them in order.

6. Replace the original array with the merged (sorted) version.

7. Display the sorted array 

8. End the program.



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
The program successfully sorts an array of integers using merge sort with recursion. When the user inputs a list of numbers, the program prints both the original (unsorted) and the sorted array.
