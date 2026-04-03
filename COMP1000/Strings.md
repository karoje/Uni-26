Strings are just a character array inside a parcel called a class. It lets us call built-in functions on variables (objects) of the String type (class).
### Declaration and initialization

```java
String str = "Kill Bill";
println(str) // displays Kill Bill
```

### Length of a string

Length of a string is given by `stringName.length()` 

### Characters in a string

The first character in a string is at index 0 like an array and we use `stringName.charAt(0)`
Last character is at `stringName.length()-1` and we use `stringName.charAt(stringName.length()-1)`

### Looping through a string

We loop through any given String `str` as:
```java 
for(int i=0; i < str.length(); i++) {
	// current character at str.charAt(i)
}
```

Examples:

Count number of spaces:
```java
int count =0;
for(int i=0; i < str.length(); i++) {
	if(str.charAt(i) == ' ') {
		count__;
	}
}
```

Count number of digits:
```java 
int count = 0;
for(int i=0; i <str.length(); i++) {
	if(str.charAt(i) >= '0' && str.charAt(i) <= '9') {
		count++;
	}
}
```

Check if purely alphabetic:
```java 
boolean stillPossible = true;
for(int i=0; i < str.length() && stillPossible; i++) {
	boolean upper = false;
	boolean lower = false;
	if(str.charAt(i) >= 'A' && str.charAt(i) <= 'Z') {
		upper = true;
	}
	if(str.charAt(i) >= 'a' && str.charAt(i) <= 'z') {
		lower = true;
	}
	if(!upper && !lower) {
	strillPossible = false
	}
}
boolean isAlpha = stillPossible;
```

### Useful functions with strings

|Function|Comment|Example|Outcome|
|---|---|---|---|
|`indexOf(another String)`|returns first index at which passed String is found, -1 if not found|1. `"its a cool tool".indexOf("ool")` 2. `"its a cool tool".indexOf("OOL")`|1. `7` 2. `-1`|
|`indexOf(char)`|returns first index at which char is found, -1 if not found|1. `"tipper".indexOf('p')` 2. `"tipper".indexOf('c')`|1. `2` 2. `-1`|
|`substring(start)`||`"superman".substring(2)`|`"perman"`|
|`substring(start, end)`|end index is not included|`"superman".substring(2, 6)`|`"perm"`|
|`toLowerCase()`|original String is NOT modified|`"Hello123!".toLowerCase()`|`"hello123!"`|
|`toUpperCase()`|original String is NOT modified|`"Hello123!".toUpperCase()`|`"HELLO123!"`|
|`Integer.parseInt(String)`|1. String is the parameter here 2. Raises exception if String not numeric|`Integer.parseInt("-4096")`|-4096|
|`equals(another String)`|1. You SHOULDN'T compare Strings using == as it checks if the two String objects being compared refer to the same instance 2. `equals` performs case-sensitive comparison|1. `"done".equals("done")` 2. `"done".equals("Done")` 3. `"ab"==new String("ab")`|1. `true` 2. `false` 3, `false`|
|`equalsIgnoreCase(another String)`|`equalsIgnoreCase` performs case-**IN**sensitive comparison|1. `"done".equals("done")` 2. `"done".equals("Done")` 3. `"done".equals("doe")`|1. `true` 2. `true` 3. `false`|
|`compareTo(another String)`|performs lexicographic (as in dictionary) comparison|1. `"Hi".compareTo("hi")` 2. `"hi".compareTo("Hi")` 3. `"what".compareTo("why?")` 4. `"why".compareTo("why")`|1. negative (exact value is irrelevant for now) 2. positive 3. negative (3rd character) 4. 0|