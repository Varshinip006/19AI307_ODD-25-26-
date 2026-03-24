# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Vehicle with attributes as number, type and owner.


## AIM:


To create a Vehicle class and store details of two vehicles (number, type, and owner) using objects, then display the entered information.



## ALGORITHM :


1.Start the program.

2.Create a class Vehicle with variables number, type, and owner.

3.In the main method, create a Scanner object to read input.

4.Create the first object v1 and read vehicle number, type, and owner.

5.Create the second object v2 and read vehicle number, type, and owner.

6.Print the details of v1 in the required format.

7.Print the details of v2 in the required format and end the program.





## PROGRAM:
 ```

Program to implement a Class and Objects using Java
Developed by: Priya Varshini P
RegisterNumber: 212224240119

import java.util.Scanner;
class Vehicle{
    String number;
    String type;
    String owner;
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Vehicle v1 = new Vehicle();
        v1.number = sc.next();
        v1.type = sc.next();
        v1.owner = sc.next();

        Vehicle v2 = new Vehicle();
        v2.number = sc.next();
        v2.type = sc.next();
        v2.owner = sc.next();

        System.out.println(v1.number + " | " + v1.type + " | " + v1.owner);
        System.out.println(v2.number + " | " + v2.type + " | " + v2.owner);

        sc.close();
    }
}


```

## OUTPUT:

<img width="932" height="280" alt="image" src="https://github.com/user-attachments/assets/ba56297d-bb85-474b-ae9f-49f50731e36c" />







## RESULT:
The program successfully reads the vehicle number, type, and owner for two vehicles and displays the details in the format:
