# Basic Java Interview Questions

Task
===

### **1. Explain JDK, JRE and JVM?**

_Java Virtual Machine(JVM)_ is used to run bytecode on every platform.
_JavaRuntime Environment (JRE)_ contains parts of the Java SE platform required to run Java programs and is intended for end users.
_Java Development Kit (JDK)_ is designed for software developers and includes development tools such as Java compiler, Javadoc, Jar and debugger.


### **2. What do you understand by Collection Framework in Java?**


The Collection in Java is a framework that provides an architecture to store and manipulate the group of objects. The collection framework includes the following:

    Interfaces
    Classes
    Algorithm


### **3. List down the primary interfaces provided by Java Collections Framework?**


_Collection Interface_: java.util.Collection is the root of the Java Collection framework and most of the collections in Java are inherited from this interface.

```public interface Collection<E>extends Iterable```

_List Interface_: java.util.List is an extended form of an array that contains ordered elements and may include duplicates. It supports the index-based search, but elements can be easily inserted irrespective of the position. The List interface is implemented by various classes such as ArrayList, LinkedList, Vector, etc.


```public interface List<E> extends Collection<E>```


_Set Interface_: java.util.Set refers to a collection class that cannot contain duplicate elements. Since it doesn’t define an order for the elements, the index-based search is not supported. It is majorly used as a mathematical set abstraction model. The Set interface is implemented by various classes such as HashSet, TreeSetand LinkedHashSet.

```public interface Set<E> extends Collection<E>```


_Queue Interface_: java.util.Queue in Java follows a FIFO approach i.e. it orders the elements in First In First Out manner. Elements in Queue will be added from the rear end while removed from the front.

```public interface Queue<E> extends Collection<E>```


Map Interface: java.util.Map is a two-dimensional data structure in Java that is used to store the data in the form of a Key-Value pair. The key here is the unique hashcode and value represent the element. Map in Java is another form of the Java Set but can’t contain duplicate elements.



### **4.  Why Collection doesn’t extend the Cloneable and Serializable interfaces?**

Collection is an abstract representation. If collection interface extends Cloneable/Serializable interfaces, then it is mandating all the concrete implementations of this interface to implement cloneable and serializable interfaces.


### ** 5. List down the major advantages of the Generic Collection.**

1. Type-safety

Suppose you want to store the name of books in ArrayList and by mistake, you added an Integer value instead if String. The Compiler allows it, but the problem occurs when you want to retrieve it. So, the compiler throws the error at run time.

By the use of generic, the compiler shows the errors at compile time rather than the run time. It saves the programmer time because it’s difficult to find the error on runtime. Its always better to find the errors at compile time rather than the run time. 

2. Typecasting is not required

If we are not using generic ArrayList, during the retrieve data from ArrayList we have to typecast it. This typecast is needed every time. It’s a big problem for programmers. So, the generic solve this problem because if we already know that, the data type list then we don’t need to cast it every time. It is the one of best advantages of generics in java.

3. Compile-Time Checking

It is checked at compile time so problem will not occur at runtime. The good programming strategy says it is far better to handle the problem at compile time than runtime.

### **6. What is the main benefit of using the Properties file?**

Recompilation is not required if the information is changed from a properties file: If any information is changed from the properties file, you don't need to recompile the java class. It is used to store information which is to be changed frequently.

### **7. What do you understand by Iterator in the Java Collection Framework?**

Iterator in Java is an interface of the Collection framework. Below are a few other major functionalities provided by the Iterator interface:

    Traverse a collection object elements one by one;
    Known as Universal Java Cursor as it is applicable for all the classes of the Collection framework;
    Supports READ and REMOVE Operations;
    Iterator method names are easy to implement.

### **8. What is the need for overriding equals() method in Java?**

The initial implementation of the equals method helps in checking whether two objects are the same or not. But in case you want to compare the objects based on the property you will have to override this method.

### **9. How the Collection objects are sorted in Java?**

Comparable and Comparator both are interfaces and can be used to sort collection elements.

| Comparable |	Comparator |
|------------|-------------|
| Comparable provides a single sorting sequence. In other words, we can sort the collection on the basis of a single element such as id, name, and price. |	The Comparator provides multiple sorting sequences. In other words, we can sort the collection on the basis of multiple elements such as id, name, and price etc. |
| Comparable affects the original class, i.e., the actual class is modified. |Comparator doesn't affect the original class, i.e., the actual class is not modified. |
| Comparable provides compareTo() method to sort elements. |	Comparator provides compare() method to sort elements.|
| Comparable is present in java.lang package.|	A Comparator is present in the java.util package.|
| We can sort the list elements of Comparable type by Collections.sort(List) method.| We can sort the list elements of Comparator type by Collections.sort(List, Comparator) method. |

### **10. What is the use of the List interface?**

The List interface provides a way to store the ordered collection.
Classes which implement the List Interface:
1. ArrayList
2. Vector
3. Stack (LIFO)

### **11. What is ArrayList in Java?**

ArrayList is the implementation of List Interface where the elements can be dynamically added or removed from the list. ArrayList in the Collection framework provides positional access and insertion of elements. It is an ordered collection that permits duplicate values. 

### **12. How would you convert an ArrayList to Array and an Array to ArrayList?**


An Array can be converted into an ArrayList by making use of the asList() method provided by the Array class. It is a static method that accepts List objects as a parameter.

Syntax:
```Arrays.asList(item)```

Whereas an ArrayList can be converted into an Array using the toArray() method of the ArrayList class.

Syntax:
```List_object.toArray(new String[List_object.size()])```

### **13. How will you reverse an List?**


ArrayList can be reversed using the reverse() method of the Collections class.

Syntax:
```public static void reverse(Collection c)```

### **14. How many types of LinkedList does Java support?**

Singly Linked List: In a singly LinkedList, each node in this list stores the data of the node and a pointer or reference to the next node in the list.

Doubly Linked List: In a doubly LinkedList, it has two references, one to the next node and another to the previous node.