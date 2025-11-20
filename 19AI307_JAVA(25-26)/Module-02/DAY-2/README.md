# Ex.No:2(B) METHODS

## QUESTION:
Write a method boolean isEven  (int num) without using % operator that returns true if the number is even.

## AIM:
To Write a method boolean isEven  (int num) without using % operator that returns true if the number is even.
## ALGORITHM :
1. Start the program and read an integer num from the user.
2. Call the function isEven(num) which checks if the number is even by using the condition:
3. Return true if the number is even, otherwise return false.
4. Print the result (true/false) to the user.
5. End the program

## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: PRAISEY S
RegisterNumber: 212222040117 
*/
```

## SOURCE CODE:
```
import java.util.*;
class prog{
    static boolean isEven(int num){
        return (num&1)==0;
    }
    public static void main(String[] args){
        Scanner s=new Scanner(System.in);
        int num=s.nextInt();
        System.out.println(isEven(num));
    }
}
```

## OUTPUT:

<img width="422" height="152" alt="image" src="https://github.com/user-attachments/assets/305b1eae-12f5-49ee-8f98-687bf6cb3a80" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.
