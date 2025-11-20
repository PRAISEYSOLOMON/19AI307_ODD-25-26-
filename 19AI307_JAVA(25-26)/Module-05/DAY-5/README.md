# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Print "Hello" and "World" alternately from two threads using synchronized blocks.
## AIM:
To write a program to print "Hello" and "World" alternately from two threads using synchronized blocks.
## ALGORITHM :
1. Start the program and read the number of repetitions from the user.
2. Create an object that controls synchronized printing of "Hello" and "World".
3. Create one thread to print "Hello" and another thread to print "World".
4. Start both threads so they run concurrently.
5. Inside the printer class, allow threads to print alternately using a shared lock and a turn-based flag.
6. Continue printing "Hello" and "World" in alternating order until both threads finish their execution.
7. End the program.
## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: PRAISEY S
RegisterNumber:  212222040117
*/
```

## SOURCE CODE:
```
import java.util.*;
class HelloWorldPrinter {
    private final Object lock = new Object();
    private boolean helloTurn = true; 

    public void printHello(int n) {
        for (int i = 0; i < n; i++) {
            synchronized (lock) {
                while (!helloTurn) { 
                    try {
                        lock.wait();
                    } catch (InterruptedException e) {
                        Thread.currentThread().interrupt();
                    }
                }
                System.out.println("Hello");
                helloTurn = false;
                lock.notifyAll();
            }
        }
    }

    public void printWorld(int n) {
        for (int i = 0; i < n; i++) {
            synchronized (lock) {
                while (helloTurn) { 
                    try {
                        lock.wait();
                    } catch (InterruptedException e) {
                        Thread.currentThread().interrupt();
                    }
                }
                System.out.println("World");
                helloTurn = true;
                lock.notifyAll();
            }
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(); // number of times to print
        HelloWorldPrinter printer = new HelloWorldPrinter();

        Thread t1 = new Thread(() -> printer.printHello(n));
        Thread t2 = new Thread(() -> printer.printWorld(n));

        t1.start();
        t2.start();
    }
}
```

## OUTPUT:

<img width="853" height="713" alt="image" src="https://github.com/user-attachments/assets/cbeafc91-d8c7-4a71-9ae8-2513e58b14c5" />

## RESULT:

The program has been executed successfully and the desired output has been obtained.
