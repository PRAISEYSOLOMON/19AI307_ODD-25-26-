# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to reverse a given string.
## AIM:
To write a Java program to reverse a given string.
## ALGORITHM :
1. Start the program and read a string from the user.
2. Initialize an empty string reversed.
3. Loop from the last character of the string to the first character.
4. Append each character to the reversed string.
5. Display the reversed string to the user.
6. End the program.

## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: PRAISEY S
RegisterNumber: 212222040117
*/
```

## SOURCE CODE:
```
import java.util.*;

public class ReverseString {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        String reversed = "";
        for (int i = str.length() - 1; i >= 0; i--) {
            reversed += str.charAt(i);
        }
        System.out.println("Reversed string: " + reversed);
    }
}
```
## OUTPUT:

<img width="722" height="247" alt="image" src="https://github.com/user-attachments/assets/c6e36261-173b-4a4e-81ec-44222b0d3ced" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.
