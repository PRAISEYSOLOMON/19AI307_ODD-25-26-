# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Develop a class with a static nested class. 
## AIM:
To write a program to develop a class with a static nested class. 
## ALGORITHM :
1. Start the program and declare static and instance variables in the outer class.
2. Define a static nested class with a method to display variable values.
3. In the nested class method, access the static variable directly, create an outer class object to access the instance variable, read a local variable, and print all values.
4. In the main method, create an object of the static nested class and call the display method.
5. End the program.

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: PRAISEY S
RegisterNumber: 212222040117 
*/
```

## SOURCE CODE:
```
import java.util.*;
public class prog{
    static int staticvar=100;
    int instancevar=200;
    static class nestedclass{
        void display(){
            Scanner s=new Scanner(System.in);
            System.out.println("Accessing static variable from outer class: "+staticvar);
            prog outer=new prog();
            System.out.println("Accessing instance variable from outer class using object: "+outer.instancevar);
            int localvar=s.nextInt();
            System.out.println("Local variable inside nested class method: "+localvar);
            
        }
    }
    public static void main(String[] args){
        prog.nestedclass nested=new prog.nestedclass();
        nested.display();
    }
}
```
## OUTPUT:

<img width="1203" height="355" alt="image" src="https://github.com/user-attachments/assets/8fa57444-c2f4-437c-b20a-02fa75b62490" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.
