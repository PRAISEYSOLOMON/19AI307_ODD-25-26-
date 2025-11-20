# Ex.No:4(D) DESIGN PATTERN -- PROTOTYPE PATTERN

## QUESTION:
You are building customizable robots using the Prototype Pattern. Clone an existing robot template and change its name and feature.
## AIM:
To implement the Prototype Design Pattern by creating a robot template that can be cloned to produce new robot objects with customized names and features.
## ALGORITHM :
1. Start the program and read the robot’s title and content from the user.
2. Create an original Document (robot template) object using the given title and content.
3. Clone the original object using the clone() method defined in the Prototype interface.
4. Display the details of the original robot.
5. Display the details of the cloned robot and end the program.
## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: PRAISEY S
RegisterNumber: 212222040117
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
interface Prototype {
    Prototype clone();
}

class Document implements Prototype {
    private String title;
    private String content;

    public Document(String title, String content) {
        this.title = title;
        this.content = content;
    }
    public Prototype clone() {
        return new Document(title, content);
    }

    public void print(String label) {
        System.out.println(label + ": " + title + " - " + content);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String title = sc.nextLine();
        String content = sc.nextLine();

        Document original = new Document(title, content);
        Document clone = (Document) original.clone();

        original.print("Original Robot");
        clone.print("Cloned Robot");
    }
}
```
## OUTPUT:

<img width="1216" height="305" alt="image" src="https://github.com/user-attachments/assets/91f35433-3578-4f3a-b2c3-381505058904" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.
