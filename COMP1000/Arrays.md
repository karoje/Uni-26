A fixed-sized collection of items, all the same data type
### Creating arrays
Option 1 (most common)
- Specify the type and size of the array

```java
type[] arrayName = new type[size];

//example

int[] arr = new int[5]; //an array that holds 5 integers
```

Option 2
- When you know the values that need to be stored
- Can't be re-referenced once created

```java
type[] arrayName = {item1, item2, ...};
```

Option 3
- Similar to option 2 except it can be re-referenced

```java
type{} arrayName = new type[]{item1, item2, ...};
```

### Size of an array
The number of items in an array is given by `arrayName.length`

### Accessing items of an array
- First item of an array is at index 0
- Second item of an array is at index 1
- Last item of an array is at index `arr.length - 1`

### Storage of an array and representation
An integer takes up 4 bytes of memory
Array items are held together in a block

Consider:

```java
int[] arr = new int[4];
```

If the first item is at memory address 200-203, the second will be at 204-207, the third at 208-211, and the last at 212-215.

The array itself holds the starting address, which is 200 in this case, hence why an array is a reference.

### Reference copy

You can copy an array (source) into another array (destination) using `=` , which will make the destination refer to the same set of items as the source.

```java
int[] a = {10, 70, 20, 90};
int[] b = a;
b[2] = -30; //a[2] is now also -30
```

### Instance copy

An instance copy is when you create an array the same size as the source array and copy everything one by one.

```java 
int[] a = {10, 70, 20, 90};
int [] c = new int[a.length];
for(int i=0; i < a.length; i++) {
	c[i] = a[i];
}
c[2] = -30; //a[2] won't get updated and will stay 20
```

