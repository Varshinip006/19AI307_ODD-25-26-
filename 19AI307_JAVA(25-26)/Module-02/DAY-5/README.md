# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".


## AIM:

To create a Java program that demonstrates the use of static methods and instance methods by performing addition using a calculator class.


## ALGORITHM :
1.Start the program.

2.Create a class Calculator with an instance method add() to add two numbers.

3.Create a static method info() to display a message that the calculator is ready.

4.In the main method, create a Scanner object to read input.

5.Call the static method Calculator.info() to display the message.

6.Create an object of the Calculator class and read two numbers from the user.

7.Call the add() method using the object to display the sum.





## PROGRAM:
 ```


Program to implement a Access Modifiers using Java
Developed by: Priya Varshini P
RegisterNumber: 212224240119
import java.util.Scanner;

class Calculator {
    void add(int a,int b)
    {
        System.out.println("Sum: "+ (a+b));
    }
    static void info()
    {
        System.out.println("Calculator is ready");
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        Calculator.info();
        Calculator c=new Calculator();
        int a=sc.nextInt();
        int b=sc.nextInt();
        c.add(a,b);
    }
}


```




## OUTPUT:

<img width="870" height="350" alt="image" src="https://github.com/user-attachments/assets/3e061ef5-2572-4ea2-bfe3-fa822e1f8571" />





## RESULT:
The program successfully displays a message using a static method and calculates the sum of two numbers using an instance method.
