# SOLID​ Design Principles

===

Acronym for 5 software design principles that help us to keep technical debt under control.

**S**ingle Responsibility Principle
**O**pen Closed Principle
**L**iskov Substitution Principle
**I**nterface Segregation Principle
**D**ependency Inversion Principle


### ** Top benefits of SOLID Code**
1. Easy to understand and reason about
2. Changes are faster and have a minimal risk level
3. Highly maintainable over long periods of time
4. Cost effective

_Single Responsibility Principle_ : every function, class or module should have one and only one reason to change.
Examples:
Business logic, user interface, persistence, logging, orchestration and users.

_Why should you use SRP?_
1. It makes code easier to understand, fix and maintain.
2. Classes are less couipled and more resilient to change
3. More testable design

```java
if(employee.getMontlyIncome() > 2000) {
    //some logic here
} else {
    //some other logic here
}```

```java
switch(employee.getNbHoursPerWork()) {
    case 40: {
        //logic for full time
    }
    case 20: {
        //logic for part time
    }
}```

```java
class ConsoleLgger {
    void logInfo (String msg) {
        system.out.println(msg);
    }

    void logError(String msg, Exception e) {...}
}
```

### **Symptoms of Not using SRP**
1. Code is more difficult to read and reason about
2. Decreased quality due to testing difficulty
3. Side effects
4. High coupling

_Coupling_ : the level of inter-dependency bettween various software components.



_Open Closed Principle_: classes, functions and modules should be closed for modification, but open for extension.

Closed for modification - each new features should not modify existing source code.
Open for extension - a component should be extendable to make it behave in new ways.

_Why should you apply the OCP?_
1. New features can be added easily and with minimal cost.
2. Minimizes the risk of regression bugs.
3. Enforces decoupling by isolating changes in specific components, works along with the SRP.

### **OCP Implementation Strategies**

_Inheritance_
```java
public class InternationalBankAccount extends BankAccount {

    @Override
    void transferMoney (double amount) {
        //business logic for international transfer
    }
}
```

or _Strategy Pattern_


_Liskov Substitution Principle_ : If S is a subtype of T, then objects of type T in a program may be 
                                    replaced with objects of type S without modifying the functionality of the program.

Any objectt of a type must be **substitutable** by objects of a derived typed without altering the correctness of that program.


_Relationships_

**Is a**
Square _is a_ kind of rectangle.
An ostrich _is a_ bird.

**Is substitutable by**
Is the class rectangle fully _substitutable by_ the class square?

```java
class Ostrich extends Bird {
    @Override public void fly(int altitude) {
        //Do nothing; An ostrich can't fly
    }
}

Bird ostrich = new Ostrich();
ostrich.fly(1000);
```


_Interface Segregation Principle_ : Clients should not be forced to depend on methods that they do not use.
The goal of the Interface Segregation Principle is to reduce the side effects and frequency of required changes by splitting the software into multiple, independent parts.

**The ISP Reinforces Other Principles**

By keeping interfaces small, the classes that implement them have a higher chance to fully subdtitute the intarface.

Classes that implement small interfaces are more focused and tend to have a single purpose.

_Dependency Inversion Principle_ : 1. **High level modules** should not depend on **low level modules**; both should depend on abstractions.
                                   2. **Abstractions** should not depend on details. Details should depend upon abstraction.


_High Level Modules_
1. Modules written to solve real problems and use cases
2. They are more abstract and map to the business domain
3. What the software should do

_Low Level Modules_
1. Contain implementation details that are required to execute the business policies
2. They are considered the "plumbing" or "internals" of an application
3. How the software should do various tasks

Examples of Low Level Modules: logging, data access, network communication, IO.

### What is Inversion of Control (IoC)?

Inversion of Control is a design principle in which the control of object creation, configuration, and lifecycle is passed to a container or framework.

IoC Container Benefits:
1. Makes it easy to switch between different implementations at runtime.
2. Increased program modularity.
3. Manages the lifesysle of objects and their configuration. 