# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to create an inner class and access it from the outer class.


## AIM:
To create a Java program that demonstrates the use of a non-static inner class and calls its method to display a message.

## ALGORITHM :
1.Start the program.

2.Create an outer class outer.

3.Inside it, create an inner class inner with a method display() to print a greeting message.

4.Create a method InnerObj() in the outer class to create an object of the inner class.

5.Call the display() method using the inner class object.

6.In the main method, read a name using Scanner.

7.Create an object of the outer class and call InnerObj() to display the message.




## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Priya Varshini P
RegisterNumber: 212224240119

import java.util.Scanner;
class outer{
    class inner{
        void display(String name){
            System.out.println("Hello, "+name+"! This message is from the Inner Class.");
        }
    }
    void InnerObj(String name)
    {
        inner o = new inner();
        o.display(name);
    }
}
public class Main{
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        outer obj = new outer();
        obj.InnerObj(name);
    }
}
*/
```




## OUTPUT:

<img width="1212" height="276" alt="image" src="https://github.com/user-attachments/assets/3c13be63-04e6-41dd-ab2b-d3666c1d685d" />



## RESULT:
The program successfully demonstrates the use of an inner class by displaying a greeting message using a method defined inside the inner class.
