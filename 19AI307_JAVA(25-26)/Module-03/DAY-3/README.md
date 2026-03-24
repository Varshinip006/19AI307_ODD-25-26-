# Ex.No:3(C) ABSTRACTION

## QUESTION:
Description:
Create abstract class GameScore with method finalScore().
Subclasses:

ArcadeGame: score = baseScore + (level × 100)

PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500

Input Format:

First line: 1 or 2
Second line: base, level (or attempts)

Output Format:

Final score (int)



## AIM:
To create a Java program that demonstrates abstraction and inheritance by calculating the final score for different types of games.



## ALGORITHM :
1.Start the program.

2.Create an abstract class GameScore with an abstract method finalScore().

3.Create a subclass ArcadeGame that calculates score as baseScore + (level × 100).

4.Create another subclass PuzzleGame that calculates score based on the number of attempts.

5.In the main method, read the game type using Scanner.

6.If type is 1, create an ArcadeGame object and calculate the score.

7.If type is 2, create a PuzzleGame object and display the final score.	





## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Priya Varshini P
RegisterNumber: 212224240119

import java.util.*;
abstract class GameScore
{
    public abstract int finalScore();
}
class ArcadeGame extends GameScore
{
    int basescore,level;
    
    ArcadeGame(int basescore,int level)
    {
        this.basescore=basescore;
        this.level=level;
    }
   public int finalScore()
    {
        return basescore+(level*100);
    }
}
class PuzzleGame extends GameScore
{
    int attempts;
    PuzzleGame(int attempts)
    {
        this.attempts=attempts;
    }
    public int finalScore()
    {
        if(attempts<=3)
             return 1000 - (attempts*100);
        else
          return 500;
          
    
        
    }
}
class prog
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int type=sc.nextInt();
        if(type==1)
        {
            int base=sc.nextInt();
            int level=sc.nextInt();
            GameScore g=new ArcadeGame(base,level);
            
            System.out.println(g.finalScore());
        }else if (type==2)
        {
            int attempts=sc.nextInt();
            GameScore g=new PuzzleGame(attempts);
            System.out.println(g.finalScore());
            
        }
    }
}
*/
```




## OUTPUT:

<img width="992" height="230" alt="image" src="https://github.com/user-attachments/assets/e58d24d5-5c1d-41ba-8834-0404a263ba38" />



## RESULT:
The program successfully calculates the final score for ArcadeGame and PuzzleGame using abstraction and method overriding.
