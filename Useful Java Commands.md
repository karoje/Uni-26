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

### Lists
`arrayList` - used for storing multiple values of the same type.
`import java.util.ArrayList;` - needs to be included at the top of the program

`ArrayList<Type> list = new ArrayList<>()` - to create a new array list
```java
// import list so that the program can use it
import java.util.ArrayList;

public class WordListExample {

    public static void main(String[] args) {
        // create the word list for storing strings
        ArrayList<String> wordList = new ArrayList<>();

        // add two values to the word list
        wordList.add("First");
        wordList.add("Second");

        // retrieve the value from position 0 of the word list, and print it
        System.out.println(wordList.get(0));
    }
}

//Output will be --- First
```
`get` method retrieves the first value from the list when it is given the parameter `0`

`list.size()` - number of elements the list contains

`for-each loop` - no separate condition for repeating or incrementing
```java
ArrayList<String> teachers = new ArrayList<>();

teachers.add("Simon");
teachers.add("Samuel");
teachers.add("Ann");
teachers.add("Anna");

for (String teacher: teachers) {
    System.out.println(teacher);
}

// Previously this would have looked like:

for (int i = 0; i < teachers.size(); i++) {
    String teacher = teachers.get(i);
    // contents of the for each loop:
    System.out.println(teacher);
}
```

`for (TypeOfVariable nameOfVariable: nameOfList)` - for-each loop definition

`list.remove()` - removes the value at the index given as the parameter
`list.remove(Integer.valueOf())` - remove a specified value from a list of integers

`list.contains()` - used to check the existence of a value in a list, receiving the value to be                                             searched as its parameter, returning a boolean 

Lists are reference type variables

### Arrays
Contains a limited number of indices for values.
Values in an array are called elements.

#### Creating an Array
1. Explicitly define size upon creation
`int[] numbers = new int[3];`

2. Provide the initial values directly with curly brackets
`int[] numbers = {10, 20, 30}`

Swapping two indices in an array:
```java
        int helper = array[swap1];
        array[swap1] = array[swap2];
        array[swap2] = helper;
```

`arrayName.length` - the length of an array

An array is a reference type
The value of the array is a reference to the information contained in the array
When used as a parameter in a method, the method receives a copy of the reference to the array

### Strings
`stringName.equals()` - used to compare strings
`stringName.split()` - takes the parameter of where to split the string. Returns an array of the                                             resulting sub-parts
`stringName.contains()` - checks if a string contains another string

`charAt` - get a character at a specified index of a string

`stringName.length()` - length of a string