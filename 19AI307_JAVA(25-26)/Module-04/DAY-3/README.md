# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).


## AIM:
To demonstrate composition (HAS-A relationship) using Library and Book classes.


## ALGORITHM :

1.Create Book class with title and author

2.Create Library class with list of books

3.Read number of books

4.For each input, create and add Book to Library

5.Display all books in library	





## PROGRAM:
 ```

Program to implement a Composition Concepts in Java
Developed by: Priya Varshini P
RegisterNumber: 212224240119
import java.util.*;

public class CompositionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();
        sc.close();
    }
}

class Book {
    private String title;
    private String author;

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return title + " by " + author;
    }
}

class Library {
    private List<Book> books = new ArrayList<>();

    public void addBook(String title, String author) {
        books.add(new Book(title, author));
    }

    public void showBooks() {
        System.out.println("Books in Library:");
        for (Book b : books) {
            System.out.println("- " + b.getDetails());
        }
    }
} 

```





## OUTPUT:

<img width="981" height="617" alt="image" src="https://github.com/user-attachments/assets/c48ffd50-536b-4b4f-88aa-9375be0a8485" />


## RESULT:
The program successfully demonstrates composition by storing and displaying books within a library.
