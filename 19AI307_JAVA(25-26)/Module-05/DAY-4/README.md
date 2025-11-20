# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for determine the priority and name of the current thread.
## AIM:
To Write a java program for determine the priority and name of the current thread.
## ALGORITHM :
1. Start the program and read a thread name from user input.
2. Get the reference of the currently running main thread.
3. Change the name of the thread to the user-given name.
4. Display the priority of the current thread.
5. Display the updated thread name.
6. Print the complete thread information.
7. End the program.

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: PRAISEY S
RegisterNumber:  212222040117
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String threadName = sc.nextLine();
        Thread t = Thread.currentThread();
        t.setName(threadName);
        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);
    }
}
```
## OUTPUT:

<img width="741" height="200" alt="image" src="https://github.com/user-attachments/assets/e3b95ee3-9ee0-4422-89a5-465361406035" />

## RESULT:

The program has been executed successfully and the desired output has been obtained.
