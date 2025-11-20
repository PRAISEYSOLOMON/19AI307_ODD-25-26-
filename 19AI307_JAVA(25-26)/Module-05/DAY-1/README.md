# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to read user input from the keyboard using InputStreamReader 
## AIM:
To Write a program to read user input from the keyboard using InputStreamReader 
## ALGORITHM :
1. Start the program.
2. Create a Scanner object to read input from the user.
3. Read a string input (the user’s name).
4. Concatenate the input with the text "Hello, " and "!".
5. Display the final greeting message on the screen.
6. End the program.

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: PRAISEY S
RegisterNumber: 212222040117
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        BufferedReader bf=new BufferedReader(new InputStreamReader(System.in));
        String str=sc.next();
        System.out.print("Hello, "+str+"!");
        
    }
}
```

## OUTPUT:

<img width="647" height="200" alt="image" src="https://github.com/user-attachments/assets/d8f03944-1675-4b28-b34f-12b2e4dcb13f" />

## RESULT:

The program has been executed successfully and the desired output has been obtained.
