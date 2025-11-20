# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Print Right-Angled Triangle Star Pattern
## AIM:
To write a program to print Right-Angled Triangle Star Pattern
## ALGORITHM :
1. Start the program and read the number of rows from the user.
2. Initialize a loop variable i from 1 to the number of rows.
3. For each value of i, run another loop j from 1 to i and print a star (*) for every iteration.
4. After printing stars for that row, move to the next line.
5. Repeat the process until all rows are printed.
6. End the program.

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: PRAISEY S
RegisterNumber: 212222040117 
*/
```

## SOURCE CODE:
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int rows = sc.nextInt();

        for (int i = 1; i <= rows; i++) {  
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```
## OUTPUT:

<img width="503" height="397" alt="image" src="https://github.com/user-attachments/assets/208f44da-17ba-40f0-a805-f5fdd6b9b2a1" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.
