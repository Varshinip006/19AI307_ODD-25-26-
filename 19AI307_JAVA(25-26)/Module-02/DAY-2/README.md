# Ex.No:2(B) METHODS

## QUESTION:

Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).


## AIM:

To create a Java program that calculates the cube of a number using methods, where the cube method internally uses the square method.


## ALGORITHM :

1.Start the program.

2.Create a class prog with two methods: square() and cube().

3.Define square(x) to return x * x.

4.Define cube(x) to return x * square(x).

5.In the main method, create a Scanner object to read input.

6.Create an object of class prog and call the cube() method with the input number.

7.Print the result and end the program.




## PROGRAM:
 ```

Program to implement a Methods using Java
Developed by: Priya Varshini P
RegisterNumber:  212224240119
import java.util.*;
class prog
{
    int square(int x)
    {
        return x*x;
    }
    int cube(int x)
    {
        return x* square(x);
    }
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        prog obj=new prog();
        System.out.println(obj.cube(n));
    }
}

```

## SOURCE CODE:







## OUTPUT:


<img width="673" height="184" alt="image" src="https://github.com/user-attachments/assets/86f55ec8-9c01-4ec9-b76d-9595c27fb3d0" />



## RESULT:
The program successfully calculates and displays the cube of the given number using the square method.
