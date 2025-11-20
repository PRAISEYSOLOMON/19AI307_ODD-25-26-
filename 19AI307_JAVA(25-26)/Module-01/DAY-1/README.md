# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Java program that demonstrates how post-increment (a++) and pre-increment (++a) operators

## AIM:
To write a Java program that demonstrates how post-increment (a++) and pre-increment (++a) operators work and to display their effects on a given number.

## ALGORITHM :
1. Start the program and read an integer input from the user.
2. Display the original number entered.
3. Apply post-increment (a++) and display the value before increment and the updated value of the variable.
4. Apply pre-increment (++a) and display the value after increment along with the updated variable.



## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: PRAISEY S
RegisterNumber: 212222040117

*/
```

## Sourcecode.java:
```
import java.util.*;
class prog{
    public static void main(String[] agrs){
        Scanner s=new Scanner(System.in);
        int num=s.nextInt();
        System.out.println("Original number = "+num);
        int num1=(num++);
        System.out.println("After post-increment (a++) = "+num1+", Now a = "+num);
        int num2=(++num);
        System.out.println("After pre-increment (++a) = "+num2+", Now a = "+num);
    }
}
```

## OUTPUT:

<img width="948" height="302" alt="image" src="https://github.com/user-attachments/assets/ac629444-e7f1-456d-aed3-3e9daaaf631c" />


## RESULT:

The program has been executed successfully and the desired output has been obtained.
