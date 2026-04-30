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

### Object-oriented programming
A class defines the attributes of objects
- i.e. the information related to them (**instance variables**)
and their commands
- i.e. their methods
The values of instance (i.e., object) variables define the internal state of an individual object, whereas methods define the functionality it offers.

An object is always instantiated by calling a method that created an object, i.e., a **constructor** by using the `new` keyword.

The class lays out the blueprint for any objects that are instantiated by it

`private` - variables are "hidden" inside the object (encapsulation)

A method is a named section of source code **inside a class**.

`static` modifier indicates that the method doesn't belong to an object and can't access any variables that belong to objects.
`static` doesn't need to be included if method is being used to process info about objects created from a given class

Instance variables are referred to with the prefix `this`.

When returning from a method, the return value has to be assigned to a variable.



If any empty line finds its way into a file, skipping an empty line can be done with `continue` and `isEmpty`.
Reading a file with try-catch and isEmpty-continue:
```java
// create a scanner to read the file text.txt
try(Scanner scanner = new Scanner(Paths.get("text.txt"))) {

	// read all the lines of the file
	while(scanner.hasNextLine()) {
		String line = scanner.nextLine();
		
		// if line is blank we do nothing
		if(line.isEmpty()) {
			continue;
		}	
		// do something with the data
	}
} catch (Exception e) {
	System.out.println("Error: " + e.getMessage());	
}
```


An **Object** refers to an independent entity that contains both data (instance variables) and behaviour (methods). 
A **Class** contains the blueprint needed to create objects, and defines the objects' variables and methods.
A class contains:
- instance variables describing the object's data
- a constructor/s used to create it
- methods that define its behaviour

We can have multiple constructors for classes, where they can take different parameters upon creation. This is known as **constructor overloading**.
- You can't have two constructors with the exact same types of parameters as Java won't be able to differentiate between them
To minimise duplicate code, you can call a constructor from within another constructor using the `this` keyword, e.g. 
```java 
public Person(String name) {
    this(name, 0);
    //here the code of the second constructor is run, and the age is set to 0
}

public Person(String name, int age) {
    this.name = name;
    this.age = age;
    this.weight = 0;
    this.height = 0;
}
```

Methods can also be overloaded in the same way e.g.
```java
public void growOlder() {
    this.age = this.age + 1;
}

public void growOlder(int years) {
    this.age = this.age + years;
}
```
The one executed depends on the parameter given.

### Primitive and reference variables

Primitive variable - information which is stored as the value of that variable
Reference variable - holds a reference to information related to that variable
- reference variables are almost always objects in Java

`toString` needs to be used for reference variables otherwise they will also print the identifier for the variable rather than just the variable. `toString` tells the program how we want the output to be printed.


`clear()` - clear an objects list