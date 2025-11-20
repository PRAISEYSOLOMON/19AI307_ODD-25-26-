# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Vehicle with attributes as number, type and owner.
## AIM:
To write a program to create a class Vehicle with attributes as number, type and owner.

## ALGORITHM :
1. Start the program and create a Scanner to read user input.
2. Create the first Vehicle object (v1) and read its number, type, and owner from the user.
3. Create the second Vehicle object (v2) and read its number, type, and owner.
4. Display the details of both vehicles
5. Close the scanner and end the program

## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: PRAISEY S
RegisterNumber: 212222040117
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class Vehicle{
    String number;
    String type;
    String owner;
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Vehicle v1 = new Vehicle();
        v1.number = sc.next();
        v1.type = sc.next();
        v1.owner = sc.next();

        Vehicle v2 = new Vehicle();
        v2.number = sc.next();
        v2.type = sc.next();
        v2.owner = sc.next();

        System.out.println(v1.number + " | " + v1.type + " | " + v1.owner);
        System.out.println(v2.number + " | " + v2.type + " | " + v2.owner);

        sc.close();
    }
}
```

## OUTPUT:

<img width="868" height="241" alt="image" src="https://github.com/user-attachments/assets/7087765d-0289-43fb-9e45-c6106b30fa50" />

## RESULT:

The program has been executed successfully and the desired output has been obtained.
