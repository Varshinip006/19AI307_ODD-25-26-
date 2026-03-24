# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to read user input from the keyboard using InputStreamReader 

## AIM:
To read input from user using BufferedReader and display output.

## ALGORITHM :

1.Create InputStreamReader object

2.Create BufferedReader object

3.Read input string from user

4.Print the input with greeting message




## PROGRAM:
 ```

Program to implement a InputStreamReader using Java
Developed by: Priya Varshini P
RegisterNumber:  212224240119

import java.io.*;

public class Main {
    public static void main(String[] args) throws Exception {
        InputStreamReader isr = new InputStreamReader(System.in);
        BufferedReader br = new BufferedReader(isr);
        
        String name = br.readLine();
        System.out.println("Hello, " + name + "!");
    }
}
```


## OUTPUT:
<img width="1220" height="225" alt="image" src="https://github.com/user-attachments/assets/30746959-8d20-451c-b700-eed856cfff60" />




## RESULT:
The program successfully reads user input and displays a greeting message.
