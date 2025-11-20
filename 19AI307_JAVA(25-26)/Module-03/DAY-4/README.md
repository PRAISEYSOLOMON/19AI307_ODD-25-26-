# Ex.No:3(D)    INTERFACE 

## QUESTION:
Schools use different grading schemes. You need to build a system to plug different strategies.

SimpleGrader: A: 90+, B: 75–89, C: 60–74, F: below 60

StrictGrader: A: 95+, B: 85–94, C: 70–84, F: below 70
## AIM:
To develop a grading system using different grading strategies (Simple and Strict) so that the final grade can be determined based on the selected grading scheme.
## ALGORITHM :
1. Start the program and read the student's marks and the grader type from the user.
2. Create a SimpleGrader object if grader type is 1, otherwise create a StrictGrader object.
3. Pass the selected grader to the GradeContext class.
4. Use the context to execute the grading strategy and compute the final grade.
5. Print the grade and end the program.
## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: PRAISEY S
RegisterNumber: 212222040117 
*/
```

## SOURCE CODE:
```
import java.util.*;

interface Grader {
    char grade(int marks);
}

class SimpleGrader implements Grader {
    public char grade(int marks) {
        if (marks >= 90) return 'A';
        else if (marks >= 75) return 'B';
        else if (marks >= 60) return 'C';
        else return 'F';
    }
}

class StrictGrader implements Grader {
    public char grade(int marks) {
        if (marks >= 95) return 'A';
        else if (marks >= 85) return 'B';
        else if (marks >= 70) return 'C';
        else return 'F';
    }
}

class GradeContext {
    private Grader grader;

    public GradeContext(Grader grader) {
        this.grader = grader;
    }

    public char executeStrategy(int marks) {
        return grader.grade(marks);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int marks = sc.nextInt();
        int graderType = sc.nextInt();
        
        Grader grader;
        if (graderType == 1)
            grader = new SimpleGrader();
        else
            grader = new StrictGrader();

        GradeContext context = new GradeContext(grader);
        System.out.println(context.executeStrategy(marks));
    }
}
```
## OUTPUT:
<img width="561" height="162" alt="image" src="https://github.com/user-attachments/assets/ffd4568e-11a7-41ee-8559-d4701616ab89" />

## RESULT:
The program has been executed successfully and the desired output has been obtained.
