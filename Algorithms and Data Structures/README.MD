### Algorithms and Data Structures


**Storing and Accessing Data**

How we can store in our application?

_The gauge reading structure:_
```java
struct Reading {
    DataTime time;
    int value;
};
```

_Read the gauge data into a variable, wait 5 seconds, repeat the read and wait process:_
```java
Reading r1 = Gauge.Read();
Thread.Sleep(5000);

Reading r2 = Gauge.Read();
Thread.Sleep(5000);

Reading r3 = Gauge.Read();
Thread.Sleep(5000);

Reading r4 = Gauge.Read();
Thread.Sleep(5000);

Reading r5 = Gauge.Read();
Thread.Sleep(5000);
```

But what happens when we stored reading all day? :arrow_right: We get a lot of information.  :arrow_right: Using a array:


1. Can contain multiple instances of a type;
2. Numeric indexing
3. Access individual items
4. Fixed size once created


Creating an Array:
```java
Reading[] reading = new Reading[5];
```
Accessing Array Data:
```java
Reading r = readings[2];
```

Updating Array Value:
```java
readings[2] = Gauge.Read();
```

**Asymptotic Analysis of Algorithms**

_Resources:_
1. Operations - the number of times we need to perform some operations
2. Memory - how much memory is consumed by the algorithms
3. Others - network transfer, compression ratios, disk usage


```java
char[] letters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
int index = 0;
while(letters[index] != 'G')
    index++;
```

**Big-O Notation**

represents _O(n)_ -  a function whose cost scales linearly with the size of the input.
Iterating over a collection of data once often indicates an O(n) algorithm.
```java
char[] letters = "abcdefghijklmnoprstuvwxyz";

for (int i = 0; i < letters.Lenght; i++) {
    Console.WriteLine(letters[i]);
}
```

_O (log n)_ - a function whose cost scales logarithmically with the input size.

_O(n^2)_ - a function that exhibits quadratic growth relative to the input size.
A doubly-nested loop is an indication that you might have an O(n^2) algorithm.
```java
void quad (char[] input, int count) {
    for (int i = 0; i < count; i+++)
        for (int x = 0; x < count; x++)
            process(input, i, x);
}
```
Really expensive and really quickly.

_O(nm)_ - a function which has two inputs that contribute to the growth.
A nested loop that iterates over two distinct collections of data might indicate an O(nm) algorithm.
```java
void nm (char[] n, int nc, char[] m, int mc) {
    for (int i = 0; i < nc; i+++)
        for (int x = 0; x < mc; x++)
            process(n[i], m[x]);
}
```

Relative Timing:

| Big-O | Elapsed Time |
|-------|--------------|
| O(1) | 1 ms|
| O(log n) | 6 ms |
| O(n) | 16.67 minutes |
| O(nm) | (16.67 * m) minutes |
| O(n^2) | 11.57 days |
| O(n^3) | 3.16888e7 years |



**Big-O** :arrow_right: Worst
**?** :arrow_right: Average
**Big-ww** :arrow_right: Best



### **Linked Lists**


_Linked List_ - a container where data is sttored in nodes consisting of a single data item and a reference to the next node.
```java
class node {
    public Node (int value) {
        this.Value = value;
        this.Next = null;
    }

    public Node Next;
    public int Value;
}
```

_Singly Linked List:_ a linked list that provides forward iteration from the start to the end of the list.
A generic class containing the data and reference tothe next node.

_Doubly Linked List:_ a linked list that provides forward iteration from the start to the end of the list, and reverse iteration, from end to start.


### **Adding Items to Linked List**

| Function | Behavior | Complexity |
|----------|----------|------------|
| AddHead | Adds a value to the beginning of the list | O(1) |
| AddTail | Adds a value at the end of the linked list | O(1) |


### **Finding Items**

| Function | Behavior | Complexity |
|----------|----------|------------|
| Find | Finds the first node whose value equals the provided argument | O(n) |
| Contains | Returns true if the specified value exists in the list, false otherwise | O(n) |


### **Removing Items**

| Function | Behavior | Complexity |
|----------|----------|------------|
| Remove | Removes the first node whose value is equal to the argument | O(n) |


### **Sorted Lists**

A double linked list where the values are inserted and stored in sort-order.

| Function | Behavior | Complexity |
|----------|----------|------------|
| Add | Addss the specified item to the linked list in the sort order of the item type. | O(n) |




### **Hash Tables**

_Associative Array_ - a collection of key/value pairs where the key can only exist once in the collection.

Examples: HTTP Headers, environment variables.

_Hash Table_ -  an associative container that provides O(1) insert, delete and search operations.
_Hash Function_ - a function that maps data of arbitrary size to data of a fixed size. It has be stability, uniformity and security.
Stability: a hash function always generates the same output given the same input.
Uniformity: a hash algorithm should distribute its resulting hash value uniformly throughout the output space.
Security: a secure hashing algorithm cannot be inverted (the input derived from the output hash).


_Hash Collision_ - when multiple distinct keys would be inserted at the same hash table index.

_Fill Factor_: the percentage of capacity representing the maximum number of entries before the table will grow.
_Growth Factor_: the multiple to increase the capacity of the hash table when the fill factor has been exceeded. 

_Hash Table Growth_:
1. Use the fill factor to determine if growth is needed
2. Use the growth factor to allocate a larger array
3. Determine the new index for the existing items in the hash table
4. Update the hash table to use the new array





### **Sorting and Searching Array Data**


**Bubble Sort**  is the simplest sorting algorithm that works by repeatedly swapping the adjacent elements if they are in wrong order.

1. Iterate - visit each item in the array from the start to the end.
2. Swap - if two neighboring items are out of order, swap them.
3. Repeat - repeat this process until the array is sorted.


Bubble Sort Asymptotic Analysis:
**Best** O(n) comparisons and swaps.
**average** O(n^2) comparisons and swaps.
**Worst** O(n^2) comparisons and swaps.
Bubble Sort's O(n^2) average case makes it a poor general-purpose sorting algorithm.

### **Insertion Sort**
Insertion Sort Asymptotic Analysis:
**Best** O(n) comparisons and swaps.
**average** O(n^2) comparisons and swaps.
**Worst** O(n^2) comparisons and swaps.

In some scenarious insertion sort can be useful.
Insertion Sort is
1. Adaptive - works well when the data is nearly sorted
2. In-place - requires only O(1) additional memory
3. Online - sorting can occur as the data is received



### **Merge Sort**

Merge Sort Asymptotic Analysis:
**Best** O(n log n) comparisons and swaps.
**average** O(n log n) comparisons and swaps.
**Worst** O(n log n) comparisons and swaps.

Merge sort has uniform algorithmic complexity in the worse, average, and best case.



### **Quicksort**


Pivot value - a value in the array where all the values to the left of the pivot are less than (or equal to) the pivot value, and all the values to the right are greater.

_Select a Pivot Value_:
1. Select a random array item
2. Select the first or last array item
3. Select the median of the first, last, and middle items


Search Algorithm - the IStringSearchAlgorithm defines the function, search, which will be called to find all of the matches of the search string (pattern) within the input (toSearch)
string.


_Boyer-Moore-Horpool_ : a 2-stage searching algorithm that uses a table that contains the length to shift when a bad match occurs.
The Boyer-Moore-Horspool is a string matching algorithm that compares characters from the end of the pattern to it is beginning. When characters do not match, searching jumps to the next matching position in the pattern. In other words, the Boyer-Moore-Horspool Algorithm is an algorithm for finding substrings into strings.


