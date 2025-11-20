# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
Write a java program to get the user input for temperature and display appropriate output.
## AIM:
To Write a java program to get the user input for temperature and display appropriate output.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Read an integer input from the user.
4. Check if the number is less than 0 → if true, print "Hibernating".
5. Else if the number is between 0 and 20 (inclusive) → print "Snoozing".
6. Else if the number is between 21 and 35 (inclusive) → print "Awake".
7. Else if the number is greater than 35 → print "Angry".
8. End the program.

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: PRAISEY S
RegisterNumber: 212222040117
*/
```

## SOURCE CODE:
```
import java.util.*;
class prog{
    public static void main(String[] args){
        Scanner s=new Scanner(System.in);
        int num=s.nextInt();
        if(num<0){
            System.out.println("Hibernating");
        }
        else if(num>=0 && num<=20){
            System.out.println("Snoozing");
        }
        else if(num>=21 && num<=35){
            System.out.println("Awake");
        }
        else if(num>35){
            System.out.println("Angry");
        }
    }
}
```

## OUTPUT:

<img width="538" height="288" alt="image" src="https://github.com/user-attachments/assets/41831ec8-20b7-4a40-9536-a1e4bc779794" />


## RESULT:
The program has been executed successfully and the desired output has been obtained.
