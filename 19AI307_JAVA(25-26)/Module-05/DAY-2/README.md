# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to simulate inter-thread communication using PipedInputStream and PipedOutputStream, where one thread writes data (input taken from the user) and another thread reads and displays the data.
## AIM:
To Write a Java program to simulate inter-thread communication using PipedInputStream and PipedOutputStream, where one thread writes data (input taken from the user) and another thread reads and displays the data.
## ALGORITHM :
1. Start the program.
2. Create and connect the PipedOutputStream and PipedInputStream.
3. Create the WriterThread and ReaderThread using the connected streams.
4. Start the ReaderThread to wait for incoming data.
5. Start the WriterThread to read user input and write it to the pipe.
6. ReaderThread reads the message from the pipe and displays it.
7. Close the streams after communication is complete.
8. End the program.

## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: PRAISEY S
RegisterNumber: 212222040117
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.Scanner;

class WriterThread extends Thread {
    private PipedOutputStream out;

    public WriterThread(PipedOutputStream out) {
        this.out = out;
    }

    @Override
    public void run() {
        try (Scanner scanner = new Scanner(System.in)) {
            String message = scanner.nextLine();

            out.write(message.getBytes());
            out.close(); 
        } catch (IOException e) {
            System.out.println("WriterThread error: " + e.getMessage());
        }
    }
}

class ReaderThread extends Thread {
    private PipedInputStream in;

    public ReaderThread(PipedInputStream in) {
        this.in = in;
    }

    @Override
    public void run() {
        try {
            byte[] buffer = new byte[1024];
            int bytesRead = in.read(buffer);
            String received = new String(buffer, 0, bytesRead);
            System.out.println("ReaderThread received: " + received);
            in.close(); 
        } catch (IOException e) {
            System.out.println("ReaderThread error: " + e.getMessage());
        }
    }
}

public class PipedCommunicationDemo {
    public static void main(String[] args) {
        try {
            PipedOutputStream out = new PipedOutputStream();
            PipedInputStream in = new PipedInputStream(out); // Connect streams

            ReaderThread reader = new ReaderThread(in);
            WriterThread writer = new WriterThread(out);

            reader.start();
            writer.start();

        } catch (IOException e) {
            System.out.println("Error in connecting pipes: " + e.getMessage());
        }
    }
}
```
## OUTPUT:

<img width="1235" height="137" alt="image" src="https://github.com/user-attachments/assets/74aa53c8-87ef-4534-92e1-bb9635da7ea7" />

## RESULT:

The program has been executed successfully and the desired output has been obtained.
