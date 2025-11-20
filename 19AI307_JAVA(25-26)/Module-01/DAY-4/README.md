# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java Program to Find the Average of Array Elements.
## AIM:
To write a Java Program to Find the Average of Array Elements.
## ALGORITHM :
1. Start the program and read the value n (number of elements).
2. Create an array of size n and set sum = 0.
3. Read each element using a loop, store it in the array, and add it to sum.
4. Calculate the average and display the value formatted to two decimal places.
5. End the program.

## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
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
        int n = sc.nextInt(); 
        int[] arr = new int[n];
        int sum = 0;
        
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
            sum += arr[i];
        }
        double average = (double) sum / n;
        System.out.printf("The average of elements is %.2f", average);
    }
}
```
## OUTPUT:

<img width="812" height="488" alt="image" src="https://github.com/user-attachments/assets/a280480d-62e1-4630-a5a9-09f5821545fa" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.
