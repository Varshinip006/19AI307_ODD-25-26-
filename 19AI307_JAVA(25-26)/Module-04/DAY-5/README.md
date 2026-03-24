# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:

Build a simple Air Traffic Control System where multiple Airplane objects request landing through a central mediator.


## AIM:

To implement Mediator Design Pattern for managing communication between airplanes using a central controller.


## ALGORITHM :

1.Create mediator interface

2.Implement mediator class (AirTrafficControl)

3.Create Airplane class with mediator reference

4.Read number of planes and condition

5.Create mediator object

6.For each plane, request landing via mediator

7.Mediator decides and displays result



## PROGRAM:
 ```

Program to implement a Behaviour Pattern using Java
Developed by: Priya Varshini P
RegisterNumber: 212224240119

import java.util.*;

interface ATCMediator {
    void requestLanding(Airplane plane);
}

class AirTrafficControl implements ATCMediator {
    private boolean multipleAllowed;
    private boolean runwayUsed = false;

    public AirTrafficControl(boolean multipleAllowed) {
        this.multipleAllowed = multipleAllowed;
    }

    public void requestLanding(Airplane plane) {
        if (multipleAllowed) {
            System.out.println(plane.getName() + " granted landing.");
            System.out.println(plane.getName() + " landed successfully.");
        } else {
            if (!runwayUsed) {
                runwayUsed = true;
                System.out.println(plane.getName() + " granted landing.");
                System.out.println(plane.getName() + " landed successfully.");
            } else {
                System.out.println(plane.getName() + " denied landing. Runway busy.");
            }
        }
    }
}

class Airplane {
    private String name;
    private ATCMediator mediator;

    public Airplane(String name, ATCMediator mediator) {
        this.name = name;
        this.mediator = mediator;
    }

    public String getName() {
        return name;
    }

    public void requestLanding() {
        mediator.requestLanding(this);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = Integer.parseInt(sc.nextLine());
        boolean multipleAllowed = Boolean.parseBoolean(sc.nextLine());

        ATCMediator atc = new AirTrafficControl(multipleAllowed);

        for (int i = 0; i < n; i++) {
            Airplane plane = new Airplane(sc.nextLine(), atc);
            plane.requestLanding();
        }

        sc.close();
    }
}

```


## OUTPUT:
<img width="1217" height="557" alt="image" src="https://github.com/user-attachments/assets/a63a8f28-323c-4a88-886a-de90c06e6da9" />





## RESULT:

The program successfully controls communication between airplanes using a mediator.
