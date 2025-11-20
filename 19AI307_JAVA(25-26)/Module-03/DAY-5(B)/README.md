# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.
## AIM:
To Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.
## ALGORITHM :
1. Read the input number and store it in a temporary variable.
2. Find the number of digits in the given number.
3. Compute the sum of each digit raised to the power of the number of digits.
4. Compare the computed sum with the original number.
5. If both match, print that it is an Armstrong number; otherwise, print that it is not.
## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
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
        int num = sc.nextInt();

        int original = num;
        int digits = Integer.toString(num).length(); 
        int sum = 0;

        while (num > 0) {
            int digit = num % 10;
            sum += Math.pow(digit, digits);
            num /= 10;
        }

        if (sum == original)
            System.out.println(original + " is an Armstrong number.");
        else
            System.out.println(original + " is not an Armstrong number.");
    }
}
```
## OUTPUT:

<img width="807" height="243" alt="image" src="https://github.com/user-attachments/assets/90b360a3-21c6-4fa2-895f-9c8d8b49d3e9" />

## RESULT:

The program has been executed successfully and the desired output has been obtained.
