Need to know:
- variables, conditions, loops
- operating on arrays
- defining and calling functions

Practise using VSCode and TMC MOOC course instead of Eclipse IDE as source codes no longer exist.

Java uses a 2 stage execution process 
1. Compile
2. Run

Anything that evaluates to a value is an **expression**
### Classes
`public static void main` goes inside your class

Class names begin with uppercase letters
Class name and file name must be identical (case sensitive)
Class contains main as the gateway method

Public = visible in the entire project
Private = only accessed within the specific class

Generally always use public.

Find the highest integer:
```java
public class myFirstJavaProject {
    public static void main(String[] args) {
        int a = 50, b = 40, c = 20;
        int max = 0;

        if(a >= b && a >= c) {
            max = a;
        }
        else {
            if(b >= a && b >= c) {
                max = b;
            }
            else { //b is not highest either, c only option
                max = c;
            }
        }
        System.out.println("Highest value: "+max); //returns "50"
    }
}
```

Find the smaller integer:
```java
public class myFirstJavaProject {
    public static void main(String[] args) {
        int x = 10, y = 20; //this is where we call our function "smaller"
        int z = smaller(x,y);
        System.out.println(z);
    }
    public static int smaller(int a, int b) {
        if(a <= b) {
            return a;
        }
        //guaranteed b is smaller than a
        else {
            return b;
        }
    }
}
```

Round off to the closest integer:
```java
public class Client {

    public static void main(String[] args) {
        System.out.println(roundOff(15.2));
        System.out.println(roundOff(-7.89));
        System.out.println(roundOff(12.5));
        System.out.println(roundOff(-30));

    }
 
    public static int roundOff(double val) {
        if(val >= 0) {
            int iPart = (int)val;
            double dPart = val - iPart;
            if(dPart < 0.5) {
                return iPart;
            }
            else {
                return iPart + 1;
            }
        }
        else {
            int iPart = (int)val;
            double dPart = val - iPart;
            if(dPart > -0.5) {
                return iPart;
            }
            else {
                return iPart -1;
            }
        }
    }
}
```

Check if same sign:
```java
public class Client {

    public static void main(String[] args) {
            boolean flag = sameSign(-4, -20);
            System.out.println(flag); //true
            System.out.println(sameSign(4, -20)); //false
            System.out.println(sameSign(-4, 20)); //false
            System.out.println(sameSign(0, -20)); //true
            System.out.println(sameSign(0, 20)); //true
    }

    /**
     * 
     * @param a
     * @param b
     * @return true if a and b both have the same sign.
     * return true if either a or b is zero.
     * return false in all other cases
     */

    public static boolean sameSign(int a, int b) {
        if(a>=0 && b>=0) {
            return true;
        }
        if(a<=0 && b<=0) {
            return true;
        }
        return false;
    }
}
```

Sum of all items in an array:
```java 
public class Client {

    public static void main(String[] args) {
            int[] data = {10,70,20,90,30,80};
            int total = sum(data);
            System.out.println("Sum of items: "+total);
    }

    public static int sum(int[] data) {
        int result = 0;
        for(int i = 0; i < data.length; i++) {
            System.out.println("interim value: "+result);
            result = result + data[i];
        }
        return result;
    }
}
```

Scanning user input and returning it:
```java
// Introduce the scanner tool used for reading user input
import java.util.Scanner;

public class Program {

    public static void main(String[] args) {
        // Create a tool for reading user input and name it scanner
        Scanner scanner = new Scanner(System.in);

        // Print "Write a message: "
        System.out.println("Write a message: ");

        // Read the string written by the user, and assign it
        // to program memory "String message = (string that was given as input)"
        String message = scanner.nextLine();

        // Print the message written by the user
        System.out.println(message);
    }
}
```

Function to find out if input is even or odd using modulo:
```java 
import java.util.Scanner;

public class OddOrEven {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);

        // Write your program here 
        // HINT:
        // You can find out if a number is even or odd using the modulo operator %
        // Take the modulo of a number and two to find out if it is even or odd!

        System.out.println("Give a number:");
        int number = Integer.valueOf(scan.nextLine());

        if( number % 2 == 0) {
            System.out.println("Number " + number + " is even.");
        } else {
            System.out.println("Number " + number + " is odd.");
        }
    }
}
```