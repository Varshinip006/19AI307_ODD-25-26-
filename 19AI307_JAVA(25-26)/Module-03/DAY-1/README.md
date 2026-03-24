# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:

finalPrice = purchaseWeight * (goldRatePerGram - discount)

For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).


## AIM:
To create a Java program that demonstrates inheritance and method overriding by calculating the final price of gold purchase for Regular and Premium customers with discounts and cashback.


## ALGORITHM :
1.Start the program.

2.Create a base class Customer with attributes: customerId, name, purchaseWeight, and goldRatePerGram.

3.Define methods to calculate discount rate, final price, and display customer details.

4.Create a subclass RegularCustomer that overrides getDiscountRate() to return 2% discount.

5.Create another subclass PremiumCustomer that overrides getDiscountRate() to return 5% discount and adds a 1% cashback method.

6.In the main method, read customer type and purchase details using Scanner.

7.Based on the customer type, create the appropriate object and display the purchase details.





## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: Priya Varshini P
RegisterNumber: 212224240119
import java.util.Scanner;
import java.text.DecimalFormat;

class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    double getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discount = goldRatePerGram * getDiscountRate() / 100;
        return purchaseWeight * (goldRatePerGram - discount);
    }

    void display(String type) {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: " + type);
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class RegularCustomer extends Customer {
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 2;
    }
}

class PremiumCustomer extends Customer {
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 5;
    }

    double getCashback() {
        return calculateFinalPrice() * 0.01;
    }

    void display(String type) {
        DecimalFormat df = new DecimalFormat("0.00");
        super.display(type);
        System.out.println("Cashback: " + df.format(getCashback()));
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String customerType = sc.next();
        String id = sc.next();
        String name = sc.next();
        double weight = sc.nextDouble();
        double rate = sc.nextDouble();

        if (customerType.equals("Regular")) {
            Customer c = new RegularCustomer(id, name, weight, rate);
            c.display("Regular");
        } else {
            PremiumCustomer c = new PremiumCustomer(id, name, weight, rate);
            c.display("Premium");
        }
    }
}

*/
```







## OUTPUT:

<img width="1044" height="713" alt="image" src="https://github.com/user-attachments/assets/2e42550d-a9a3-4822-87c6-805369bebc5a" />




## RESULT:
The program successfully calculates the final price of gold purchase with discounts for Regular and Premium customers and also displays cashback for Premium customers.
