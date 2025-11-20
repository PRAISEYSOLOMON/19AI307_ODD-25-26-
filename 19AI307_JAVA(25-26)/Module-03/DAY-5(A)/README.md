# Ex.No:3(E) INNER CLASS

## QUESTION:
Write an enum Grade with constants A, B, C, D, F. Assign a message like "Excellent" for A and "Good" for B and "Average" for C and "Fail" for F using constructor. Display grade with message.
## AIM:
To create an enum Grade with constants A, B, C, D, and F, each having an associated message using a constructor, and to display the grade along with its message.
## ALGORITHM :
1. Start the program and read a grade letter from the user.
2. Convert the input to uppercase and match it with the corresponding enum constant.
3. If the grade exists, retrieve its associated message using the enum’s constructor and display both the grade and message.
4. If the input does not match any enum constant, display “Invalid grade!”.
5. End the program.
## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: PRAISEY S
RegisterNumber: 212222040117 
*/
```

## SOURCE CODE:
```
import java.util.*;

enum Grade {
    A("Excellent"),
    B("Good"),
    C("Average"),
    D("Poor"),
    F("Fail");

    private String message;

    Grade(String message) {
        this.message = message;
    }

    public String getMessage() {
        return message;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine().toUpperCase();

        try {
            Grade grade = Grade.valueOf(input);
            System.out.println("Grade: " + grade + " - " + grade.getMessage());
        } catch (IllegalArgumentException e) {
            System.out.println("Invalid grade!");
        }
    }
}
```
## OUTPUT:

<img width="686" height="246" alt="image" src="https://github.com/user-attachments/assets/a0b642e5-d3e0-4991-916b-6be0a57ef430" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.
