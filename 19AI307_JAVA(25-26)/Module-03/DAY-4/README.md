# Ex.No:3(D)    INTERFACE 

## QUESTION:
You're building the equalizer system for a music app like BeatBoxx. The equalizer has 3 basic sound modes:

BassBoost
VocalBoost
Balanced
Each mode behaves differently and alters the sound experience. The app uses a SoundMode interface that each mode implements.

Input Format:
One line: Mode name (bass/vocal/balanced)

Output Format:
Display settings applied message for that mode

bass -  Print  "Bass Boost applied. Feel the beat drop!"

vocal - Print  "Vocal Boost enabled. Enjoy crystal-clear lyrics!"

balanced - Print  "Balanced mode set. A perfect blend of bass and vocals."
 else - Print "Invalid mode selected."

## AIM:
To create a Java program that demonstrates the use of interfaces and polymorphism by implementing different sound modes in a music system.


## ALGORITHM :
1.Start the program.

2.Create an interface SoundMode with a method display().

3.Create classes BassBoost, VocalBoost, and Balanced that implement the SoundMode interface.

4.Define the display() method in each class to print the respective sound mode message.

5.In the main method, read the sound mode from the user using Scanner.

6.Based on the input, create the appropriate object and call the display() method.

7.If the input does not match any mode, print "Invalid mode selected."	





## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Priya Varshini P
RegisterNumber: 212224240119

import java.util.*;
interface SoundMode
{
    void display();
}
class BassBoost implements SoundMode{
    public void display()
    {
        System.out.println("Bass Boost applied. Feel the beat drop!");
    }
        
    
}
class VocalBoost implements SoundMode{
    public void display()
    {
        System.out.println("Vocal Boost enabled. Enjoy crystal-clear lyrics!");
    }
}
class Balanced implements SoundMode{
    public void display()
    {
        System.out.println("Balanced mode set. A perfect blend of bass and vocals.");
    }
}
public class prog
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        String mode=sc.nextLine();
        SoundMode sm;
        if(mode.equalsIgnoreCase("bass"))
        {
            sm=new BassBoost();
            sm.display();
        }else if(mode.equalsIgnoreCase("vocal"))
        {
            sm=new VocalBoost();
            sm.display();
        }else if(mode.equalsIgnoreCase("balanced"))
        {
            sm=new Balanced();
            sm.display();
        }
        else
        {
            System.out.println("Invalid mode selected.");
        }
        sc.close();
    }
}
*/
```





## OUTPUT:

<img width="1247" height="211" alt="image" src="https://github.com/user-attachments/assets/35df6f9b-8479-4755-9e14-f06231d734ac" />



## RESULT:
The program successfully demonstrates interface implementation and runtime polymorphism by selecting and displaying the appropriate sound mode message.
