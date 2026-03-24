# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a java program to find the longest word in a sentence.

## AIM:

To write a Java program to find the longest word in a given sentence.

## ALGORITHM :

1.Start the program.

2.Import the required Java utility package.

3.Create a Scanner object to read input from the user.

4.Read a sentence from the user.

5.Split the sentence into words using the split() method.

6.Assume the first word as the longest word.

7.Use a loop to check each word in the sentence.

8.Compare the length of each word with the current longest word.

9.If a word is longer, update the longest word.

10.After checking all words, print the longest word.



## PROGRAM:

 ```java
import java.util.*;
class prog
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        String s=sc.nextLine();
        String[] words=s.split(" ");
        String longest=words[0];
        for(int i=1;i<words.length;i++)
        {
            if(words[i].length()>longest.length())
            {
                longest=words[i];
            }
        }
        System.out.println("The longest word is: "+longest);
        
    }
}
```

## SOURCE CODE:







## OUTPUT:

<img width="1106" height="317" alt="image" src="https://github.com/user-attachments/assets/fae97b8c-f1b0-4a0f-9263-45bfa0fe06ba" />




## RESULT:
Thus, the Java program to find the longest word in a given sentence was executed successfully and the output was obtained.

