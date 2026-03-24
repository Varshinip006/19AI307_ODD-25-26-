# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:

You have a program that reads an integer from the user. The program must reject any negative number by throwing a special error.How would you design a custom exception to handle this? What message would you display if the user enters a negative number?


## AIM:

To create and handle a custom exception in Java for negative number input.



## ALGORITHM :

1.Create a custom exception class for negative numbers
   
2.Read an integer input from user

3.Check if the number is less than 0

4.If negative, throw custom exception with message

5.Else, print the valid number

6.Catch the exception and display the error message

7.Close the scanner



## PROGRAM:
 ```

Program to implement a Exception Handling using Java
Developed by: Priya Varshini P
RegisterNumber:  212224240119
import java.util.Scanner;
class NegativeNumberException extends Exception {
    public NegativeNumberException(String message) {
        super(message);
    }
}


public class CustomExceptionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int number = sc.nextInt();

        try {
            if (number < 0) {
                throw new NegativeNumberException("Negative numbers are not allowed");
            } else {
                System.out.println("Valid input: " + number);
            }
        } catch (NegativeNumberException e) {
            System.out.println(e.getMessage());
        }

        sc.close();
    }
}
```




## OUTPUT:
<img width="1272" height="305" alt="image" src="https://github.com/user-attachments/assets/d3e0f424-3dda-43db-aef1-49c7f2b559a5" />




## RESULT:
The program successfully detects negative input and displays a custom exception message, otherwise prints the valid number.
