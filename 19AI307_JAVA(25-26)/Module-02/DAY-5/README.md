# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Student with variables name, rollNumber. Create a method setDetails(String name, int rollNumber),and display them.

## AIM:
To write aprogram to create a class Student with variables name, rollNumber. Create a method setDetails(String name, int rollNumber),and display them.
## ALGORITHM :
1. Start the program and read the student’s name and roll number from the user.
2. Create a Student object.
3. Store the entered details in the object using the setDetails method.
4. Display the stored name and roll number using the display method.
5. End the program.

## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: PRAISEY S
RegisterNumber: 212222040117 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Student {
    String name;
    int rollNumber;
    void setDetails(String name, int rollNumber) {
        this.name = name;
        this.rollNumber = rollNumber;
    }
    void display() {
        System.out.println("Name: " + name);
        System.out.println("Roll Number: " + rollNumber);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        String name = sc.nextLine();
        int rollNumber = sc.nextInt();
        
        Student s1 = new Student();
        s1.setDetails(name, rollNumber);
        s1.display();
    }
}
```
## OUTPUT:

<img width="626" height="281" alt="image" src="https://github.com/user-attachments/assets/efe02f1f-f66f-4eb2-99a3-ce0cef4f2610" />

## RESULT:

The program has been executed successfully and the desired output has been obtained.
