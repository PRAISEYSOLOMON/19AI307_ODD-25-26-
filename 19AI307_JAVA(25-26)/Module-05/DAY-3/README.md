# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Read a file and reverse the order of words in each line.
## AIM:
To write a program to read a file and reverse the order of words in each line.
## ALGORITHM :
1. Start the program.
2. Read input lines from the user continuously.
3. If the input line is "exit", stop the program.
4. If the line is empty, skip it and read the next line.
5. Split the line into words.
6. Reverse the order of the words.
7. Print the reversed words as a new line.
8. Repeat until "exit" is entered.
9. End the program.
## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: PRAISEY S
RegisterNumber:  212222040117
*/
```

## SOURCE CODE:
```
import java.util.*;

public class ReverseWordsInFile {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Reversed lines: ");
        while (sc.hasNextLine()) {
            String line = sc.nextLine();
            if (line.trim().equals("exit")) break;
            if (line.trim().isEmpty()) continue;
            String[] words = line.split("\\s+");
            StringBuilder reversed = new StringBuilder();
            for (int i = words.length - 1; i >= 0; i--) {
                reversed.append(words[i]);
                if (i != 0) reversed.append(" ");
            }
            System.out.println(reversed.toString());
        }
        sc.close();
    }
}
```
## OUTPUT:

<img width="867" height="336" alt="image" src="https://github.com/user-attachments/assets/af80778d-c1cb-4084-93a2-a2191924a070" />

## RESULT:

The program has been executed successfully and the desired output has been obtained.
