# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
Create a food delivery system using inheritance. The base class Order contains orderId, customerName, totalAmount, and deliveryCharge. Two subclasses are derived:

NormalUser → pays full delivery charge.
finalAmount = totalAmount + deliveryCharge

PrimeUser → gets 50% discount on delivery charge.
finalAmount = totalAmount + (deliveryCharge × 0.5)

The program should read three orders.
Each order input includes: user type ("Normal" or "Prime"), orderId, customerName, totalAmount, and deliveryCharge.
For each order, calculate the final amount based on user type and display all order details.

## AIM:
To develop a food delivery management program using inheritance that processes orders from Normal and Prime users and calculates the final payable amount based on their delivery charge benefits.

## ALGORITHM :
1. Start the program and read three orders from the user.
2. For each order, read the user type, order ID, customer name, total amount, and delivery charge.
3. Create a NormalUser object if the user type is "Normal", otherwise create a PrimeUser object.
4. Calculate the final amount using the formula defined in the respective subclass.
5. Display all order details including final payable amount.
6. Repeat the process for all three orders and end the program.
## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: PRAISEY S
RegisterNumber: 212222040117 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
import java.text.DecimalFormat;

class Order {
    String orderId;
    String customerName;
    double totalAmount;
    double deliveryCharge;

    public Order(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        this.orderId = orderId;
        this.customerName = customerName;
        this.totalAmount = totalAmount;
        this.deliveryCharge = deliveryCharge;
    }

    double calculateFinalAmount() {
        return totalAmount + deliveryCharge;
    }

    void display(String userType) {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Order ID: " + orderId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("User Type: " + userType);
        System.out.println("Total Amount: " + totalAmount);
        System.out.println("Delivery Charge: " + deliveryCharge);
        System.out.println("Final Amount: " + df.format(calculateFinalAmount()));
    }
}

class NormalUser extends Order {
    public NormalUser(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        super(orderId, customerName, totalAmount, deliveryCharge);
    }

    @Override
    double calculateFinalAmount() {
        return totalAmount + deliveryCharge;
    }

    @Override
    void display(String userType) {
        super.display("Normal");
    }
}

class PrimeUser extends Order {
    public PrimeUser(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        super(orderId, customerName, totalAmount, deliveryCharge);
    }

    @Override
    double calculateFinalAmount() {
        return totalAmount + (deliveryCharge * 0.5);
    }

    @Override
    void display(String userType) {
        super.display("Prime");
    }
}

public class FoodDeliveryApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int count = 0;
        while (count < 3 && sc.hasNext()) {
            String userType = sc.next();
            String orderId = sc.next();
            String customerName = sc.next();
            double totalAmount = sc.nextDouble();
            double deliveryCharge = sc.nextDouble();

            Order order;
            if (userType.equalsIgnoreCase("Normal")) {
                order = new NormalUser(orderId, customerName, totalAmount, deliveryCharge);
                order.display("Normal");
            } else if (userType.equalsIgnoreCase("Prime")) {
                order = new PrimeUser(orderId, customerName, totalAmount, deliveryCharge);
                order.display("Prime");
            }

            count++;
        }

        sc.close();
    }
}
```

## OUTPUT:

<img width="878" height="620" alt="image" src="https://github.com/user-attachments/assets/7cabd83c-9787-40d9-913f-4acdebcc3317" />

## RESULT:

The program has been executed successfully and the desired output has been obtained.
