# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a large office, multiple departments send print jobs to a shared central printer. To manage load and prevent collision, a Print Spooler Manager handles all job submissions.

The IT team insists that there should be only one spooler manager instance in the entire system. Regardless of how many jobs or departments exist, all jobs must pass through this one manager.

Your task is to simulate a singleton print job queue. Each print job submitted increases the queue count.
## AIM:
To implement a Singleton Print Spooler Manager in Java that ensures only one instance handles all print job submissions, and to simulate a centralized print job queue where each new job increases the queue count.
## ALGORITHM :
1. Read the number of print job requests.
2. For each request, read the department name.
3. Access the single shared instance of PrintSpoolerManager using getInstance().
4. Submit the print job and increase the job counter.
5. Display the department name and the updated total job count.

## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: PRAISEY S
RegisterNumber: 212222040117 
*/
```

## SOURCE CODE:
```
import java.util.*;

class PrintSpoolerManager {
    private static PrintSpoolerManager instance; 
    private int jobCount; 
    private PrintSpoolerManager() {
        jobCount = 0;
    }
    public static PrintSpoolerManager getInstance() {
        if (instance == null) {
            instance = new PrintSpoolerManager();
        }
        return instance;
    }
    public int submitJob(String department) {
        jobCount++;
        return jobCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String dept = sc.nextLine();
            PrintSpoolerManager spooler = PrintSpoolerManager.getInstance(); 
            int total = spooler.submitJob(dept);
            System.out.println(dept + " submitted a print job. Total Jobs in Queue: " + total);
        }
    }
}

```
## OUTPUT:
<img width="1150" height="391" alt="image" src="https://github.com/user-attachments/assets/9b631d8c-be29-4e40-bb06-41b827826c07" />

## RESULT:

The program has been executed successfully and the desired output has been obtained.
