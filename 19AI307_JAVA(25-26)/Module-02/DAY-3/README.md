# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.
## AIM:
To Write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.
## ALGORITHM :
1. Start the program and create a Scanner to read user input.
2. Create a Bank Account object using the bankacc class.
3. Read the account number from the user and store it using the setaccno() method.
4. Read the balance from the user and store it using the setbalance() method.
5. Retrieve and display the stored account number using getaccno().
6. Retrieve and display the stored balance using getbalance().
7. End the program.

## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: PRAISEY S
RegisterNumber: 212222040117 
*/
```

## SOURCE CODE:
```
import java.util.*;
class bankacc{
    private String accno;
    private double balance;
    public String getaccno(){
        return accno;
    }
    public void setaccno(String accno){
        this.accno=accno;
    }
    public double getbalance(){
        return balance;
    }
    public void setbalance(double balance){
        this.balance=balance;
    }
}
public class prog{
    public static void main(String[] args){
        Scanner s=new Scanner(System.in);
        bankacc account=new bankacc();
        String accno=s.nextLine();
        account.setaccno(accno);
        double bal=s.nextDouble();
        account.setbalance(bal);
        System.out.println("Account Number: "+account.getaccno());
        System.out.println("Balance: "+account.getbalance());
    }
}
```
## OUTPUT:

<img width="872" height="372" alt="image" src="https://github.com/user-attachments/assets/ebb24864-3744-48ab-aaf2-8dad132efdd1" />

## RESULT:

The program has been executed successfully and the desired output has been obtained.
