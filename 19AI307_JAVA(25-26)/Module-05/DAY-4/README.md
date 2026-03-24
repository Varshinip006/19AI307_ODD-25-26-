# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2

Note : Read the threadname from the User

set the priority as 4 for t1 and set the priority as 2 for t2



## AIM:


## ALGORITHM :

1.Create a class extending Thread

2.Read thread names from user

3.Create thread objects

4.Set priority for each thread

5.Display thread details



## PROGRAM:
 ```

Program to implement a Thread Priority Concept using Java
Developed by: Priya Varshini P
RegisterNumber:  212224240119

import java.util.Scanner;

class MyThread extends Thread {
    public MyThread(String name) {
        super(name); 
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name1 = sc.nextLine();
        String name2 = sc.nextLine();

        MyThread t1 = new MyThread(name1);
        MyThread t2 = new MyThread(name2);
        t1.setPriority(4);
        t2.setPriority(2);

        System.out.println(t1);
        System.out.println(t2);

        sc.close();
    }
}
```



## OUTPUT:

<img width="1255" height="262" alt="image" src="https://github.com/user-attachments/assets/05c22b08-77ef-40a0-a15e-f35832aca44d" />



## RESULT:

The program successfully creates threads and displays their details with assigned priorities.
