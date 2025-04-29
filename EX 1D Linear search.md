# EX 1D Linear search
## DATE: 25-02-2025
## AIM:
To write a Python program that defines a search function to find a value in a list of integers, using the list and search value as parameters.

## Algorithm
1. Start the program.

2. Define a function search(List, n) to search for value n in the list List.

3. Loop through each element in the list.

4. Compare each element with n.

5. Return True if a match is found.

6. Return False after the loop ends if no match is found.

7. Display "Found" if search returns True; otherwise, display "Not Found".

8. End the program

## Program:
```
/*
Program to implement a search function with parameter list name and the value to be searched using string values.
Developed by: RAMYA R
Register Number:  212223230169
*/

def search(List, n):
    for i in range(len(List)):
        if List[i] == n:
            return True
    return False
    
List =[]    
x=int(input())
for i in range(x):
    List.append(input())

n = input()
if search(List, n):
    print("Found")
else:
    print("Not Found")
```

## Output:

![image](https://github.com/user-attachments/assets/6fd96728-6cc7-4994-a051-1a5431a8fd58)


## Result:
The program successfully implements a search function to check whether a given integer exists in a list. It accepts a list of integers and a value to search, then prints "Found" if the value exists in the list, and "Not.
