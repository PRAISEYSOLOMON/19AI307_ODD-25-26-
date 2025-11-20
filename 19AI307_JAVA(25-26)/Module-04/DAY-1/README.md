# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You are writing a Java program where you read a string input. If the input is "init", you create an object and call its method. If it's "null", no object is created. Your program crashes with a NullPointerException when "null" is entered.
## AIM:
To write a Java program that safely handles string input and prevents a NullPointerException by checking whether an object should be created before calling its methods.
## ALGORITHM :
1. Read the input string from the user.
2. Check if the input is "null"; if true, throw a NullPointerException.
3. If the input is not "null", display that the object exists.
4. Catch the NullPointerException and print that the object is null.
5. End the program.
## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: PRAISEY S 
RegisterNumber: 212222040117 
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        try{
            String input=sc.next();
            if(input.equals("null"))
            {
                throw new NullPointerException();
            }
            else
            {
                System.out.print("Object exists");
            }
        }
        catch(NullPointerException e)
        {
            System.out.println("Object is null");
        }
    }
}
```
## OUTPUT:

<img width="777" height="247" alt="image" src="https://github.com/user-attachments/assets/f75c4f7b-52a3-4375-94f2-04b834f7b1c3" />

## RESULT:

The program has been executed successfully and the desired output has been obtained.
