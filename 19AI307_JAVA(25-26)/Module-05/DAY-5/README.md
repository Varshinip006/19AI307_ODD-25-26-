# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:

Use a synchronized block (not method) to safely increment a shared counter using multiple threads.


## AIM:
To implement multithreading with synchronization for safe increment of a shared variable.


## ALGORITHM :

1.Create Counter class with variable

2.Create Worker thread class

3.Use synchronized block to increment count

4.Read number of threads and increments

5.Create and start threads

6.Wait for threads using join()

7.Display final count



## PROGRAM:
 ```

Program to implement a Synchronization concept using Java
Developed by: Priya Varshini P
RegisterNumber: 212224240119
import java.util.*;

class Counter {
    int count = 0;
}

class Worker extends Thread {
    Counter counter;
    int times;

    Worker(Counter counter, int times) {
        this.counter = counter;
        this.times = times;
    }

    public void run() {
        for (int i = 0; i < times; i++) {
            synchronized(counter) {
                counter.count++;
            }
        }
    }
}

public class Main {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        int threads = sc.nextInt();
        int increments = sc.nextInt();

        Counter counter = new Counter();
        Worker[] w = new Worker[threads];

        for (int i = 0; i < threads; i++) {
            w[i] = new Worker(counter, increments);
            w[i].start();
        }

        for (int i = 0; i < threads; i++) {
            w[i].join();
        }

        System.out.println("Final count: " + counter.count);
    }
}

```



## OUTPUT:

<img width="1252" height="326" alt="image" src="https://github.com/user-attachments/assets/fe6cc168-7a98-4579-b724-e2e5e37e009c" />




## RESULT:

The program successfully increments a shared counter using multiple threads without race conditions.
