We will often pass arrays to functions so they can be operated on, modified, or returned. 

### Operating on an array passed to a function

When you pass an array to a function, a reference copy of the actual parameter is made into the formal parameter. In the below example, `data` becomes a reference copy of `arr`.

```java 
void caller() {
	int[] arr = {10, 70, 50};
	int sum = total(arr);
}

int total(int[] data) {
	int result = 0;
	for(int i=0; i < data.length; i++) {
		result+=data[i];
		}
	return result;
}
```

### Modifying contents of an array

If you have a function that modifies the passed array, the contents of the actual parameter will also change

```java
void caller() {
	int[] arr = {10, -70, 0};
	negate(arr);
}

void negate (int[] data) {
	for(int i=0; i < data.length; i++) {
		data[i]=data[i]*-1;
		}
}
```


