# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to count the number of characters in a file.


## AIM:
To write data into a file and count the number of characters using FileWriter and FileReader.


## ALGORITHM :

1.Read input text from user

2.Write text to file using FileWriter

3.Close the file

4.Open file using FileReader

5.Read characters one by one

6.Count total characters

7.Display count



## PROGRAM:
 ```

Program to implement a File Handling using Java
Developed by: Priya Varshini P
RegisterNumber:  212224240119

import java.io.*;
import java.util.*;

public class Main {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        String text = sc.nextLine();

        FileWriter fw = new FileWriter("data.txt");
        fw.write(text);
        fw.close();

        FileReader fr = new FileReader("data.txt");
        int count = 0;
        while (fr.read() != -1) {
            count++;
        }
        fr.close();

        System.out.println("Number of characters written to the file: " + count);
    }
}
```


## OUTPUT:

<img width="1197" height="267" alt="image" src="https://github.com/user-attachments/assets/a4299130-f665-49f2-8b61-1b4a5bb73bd7" />




## RESULT:

The program successfully writes data to a file and counts the number of characters.
