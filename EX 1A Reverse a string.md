# EX 1A Reverse a String
## DATE: 25-02-2025
## AIM:
To write a program to create a recursive function to reverse a string.

## Algorithm
1. Start the program.

2. Define a recursive function reverse_string(s) that takes a string s as input.

3. Check if the length of s is 0 (base case):  If yes, return the empty string.

4. If not, extract the last character of the string using s[-1].

5. Call the function recursively with the rest of the string s[:-1] (excluding the last character).

6. Concatenate the last character with the result of the recursive call.

7. Take input from the user and pass it to the recursive function.

8. Print the reversed string.

9.End the program.  

## Program:
```
/*
Program to implement Reverse a String
Developed by: RAMYA R
Register Number:  212223230169
*/

def reverse_string(s):
    if len(s) == 0:
        return s
    else:
        return s[-1] + reverse_string(s[:-1])
        
user_input = input()        
reversed_str = reverse_string(user_input)
print(reversed_str)
```

## Output:

![image](https://github.com/user-attachments/assets/1dfd91f3-57b7-4bcd-b8eb-7fbdb51486f6)


## Result:
The program successfully reverses the input string using recursion. When the user provides an input string, the output displays the reversed version of the string
