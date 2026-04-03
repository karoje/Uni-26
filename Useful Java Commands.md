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