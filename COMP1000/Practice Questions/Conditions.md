1. What is the value of result when the following code is executed?
```java
float result = 1.5;
int a = 12, b = 5;
if(b > a) {
	result += 0.3;
} else { 
	result -= 0.3;
}
```
	result = 1.2

2. What is the value of result when the following code is executed? 
```java
float result = 1.5;
int a = 12, b = 5;
if(a % b == a / b) {
	result += 0.3;
} else { 
	result -= 0.3;
}
```
	result = 1.8

3. What is the value of result when the following code is executed, if, 
	1. a = 7, b = 12
	2. a = 15, b = 12
	3. a = 12, b = 12
```java 
int result = 4;
if(b > a) {
	result = 1;
} else if (b < a) {
	result = -1;
} else {
	result = 0;
}
```

4. For what range of marks, will the value of result when the following code is executed, be 2? 
```java 
int result = 0;
int marks = (int)random(101); //between 0 and 100
if(marks < 50) {
	result = 0;
} else if(marks < 65) {
	result = 1;
} else if(marks < 75) {
	result = 2;
} else if(marks < 85) {
	result = 3;
} else {
	result =4;
}
```

5. Assuming the existence of an integer variable data with some value stored in it, write a piece of code that assigns the absolute value of data into another integer variable result.
6. Assuming the existence of two integer variables a, b with some values stored in them, write a piece of code that assigns, to a third integer variable result,
	1. 1 if both a, b are positive
	2. -1 if both a, b are negative
	3. 0 in all other cases
7. Assuming the existence of two integer variables a, b with some values stored in them, write a piece of code that assigns, to a third integer variable result,
	1. 1 if both a, b are even
	2. -1 if both a, b are odd
	3. 0 in all other cases
8. Assuming the existence of an floating-point variable data with some value stored in it, write a piece of code that assigns, to a second integer variable result, the value of data rounded-off to the nearest integer. For example, if data = 4.6, result should be 5. If data = 4.4, results should be 4. If data = 4.5, result should be 5. If data = 4.0, result should be 4. 