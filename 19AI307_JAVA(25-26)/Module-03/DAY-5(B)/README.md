# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is prime using wrapper classes. 

## AIM:
To create a Java program that checks whether a given number is a prime number using wrapper class Integer.


## ALGORITHM :
1.Start the program.

2.Create a Scanner object to read input from the user.

3.Convert the input string into an Integer using Integer.valueOf().

4.Assume the number is prime by setting isPrime = true.

5.If the number is less than or equal to 1, mark it as not prime.

6.Use a loop from 2 to num/2 to check if the number is divisible by any value.

7.If divisible, set isPrime to false and print the appropriate message.





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Priya Varshini P
RegisterNumber: 212224240119

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Integer num = Integer.valueOf(sc.nextLine());
        boolean isPrime = true;

        if (num <= 1) {
            isPrime = false;
        } else {
            for (Integer i = 2; i <= num / 2; i++) {
                if (num % i == 0) {
                    isPrime = false;
                    break;
                }
            }
        }

        if (isPrime) {
            System.out.println(num + " is a prime number.");
        } else {
            System.out.println(num + " is not a prime number.");
        }
    }
}
*/
```





## OUTPUT:

<img width="831" height="277" alt="image" src="https://github.com/user-attachments/assets/746aba46-3e05-4851-9424-ff6df2b47072" />



## RESULT:
The program successfully determines whether the given number is prime or not and displays the result.
