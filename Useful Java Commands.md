`scanner.nextLine()` - Scans text inputted by the user

`Integer.valueOf()`  - Converts a string to an integer
				 - Parameter is the string containing the value to be converted
```java
//Example of string to integer conversion
String valueAsString = "42";
int value = Integer.valueOf(valueAsString);

System.out.println(value);
```
`Double.valueOf()`  - Converts a string to a double
`Boolean.valueOf()` - Converts a string into a boolean

`Alt + Shift + F` --> Fix Indentation

`variable.equals` to check equivalence of two strings
```java 
String input = scanner.nextLine();
String output = scanner.nextLine();

input.equals(output);
input.equals("a string"); //can also compare against a partial string
```

`break` - used to stop a loop from executing
`continue` - will go back to the beginning of a loop

```java
for (*introducing a variable*; *condition*; *increasing the counter*) {
	//functionality to be executed	
}
```

### Methods
Written outside main but inside the class. 
A piece of a program that can be called from elsewhere
```java
public class Example {
    public static void main(String[] args) {
        // program code
    }

    // your own methods here
}
```

Method parameters are distinct from the variables (or parameters) of other methods, even if they have the same name.

If a method does not return a value - use **void** in the definition.
`void` = method returns nothing
```java
public static int alwaysReturnsTen() {
    return 10;
}
```
Declare the type of return variable in the definition if the method needs to return something