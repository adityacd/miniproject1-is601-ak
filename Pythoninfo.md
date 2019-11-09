# Information about Python
# There are some important terminology in python which evryone needs to know, which are as follows:-

**1. How python uses indentation to control flow:-**
Python uses whitespace character or spaces as indentation tools to implement control flow. It helps our ability ability to write code   that is useful.
```
# example showing that Python uses whitespace to delimit scope
x = 1

if x > 10:
    # we are inside the if-block; this line starts with four blank spaces
    x = x + 1
# we are outside of the if-block; there are no leading whitespace characters
x = x + 3
```

**2. Don’t repeat yourself:-**
DRY or don’t repeat yourself is a basic code of conduct of writing code whose aim is to reduce redundancy caused by repetition of software patterns. 

**3. Design patterns from Gang Of Four:-**
The design patterns from Gang Of Four are based on object oriented programming and can be applied to any object oriented languages like java , C++. The gang of four patterns are broken into three categories 
a)Creational design patterns
b)Structural design patterns
c)Behavioural design patterns
```
a)Types of creational design patterns:-
-Abstract factory
-Builder
-Factory model
-Prototype
-Singleton

b)Types of structural design patterns:-
-Adapter
-Bridge
-Composite
-Decorator
-Facade
-Flyweight
-Proxy

c)Types of behavioural design patterns:-
-Chain of responsibilty
-Command
-Interpreter
-Iterator
-Mediator
-Memento
-Observer
-State
-Strategy
-Template Method
-Visitor
```

**4. Class:-**
A class in python is basically an object constructor or a blueprint for creating objects.
```Following is an example of class:-
class Web_Systems_Development:
x = 6
```

 **5. Objects:-**
Object is an element of a class, and it has the behaviour of it’s class.

**6. Static:-** 
A static is a method which is bound to a class, rather than the objects for that class. It can be called without an object.

**7. Property/Attribute:-** 
An attribute belongs to a class itself and it is shared by all instances of that class, it is defined in the class body at the top. Instance attributes are not are not shared by objects.

**8. Method:-** 
Method is a function that is available for an object due to the object’s type and it is a member of the class.

**9. Exception:-**
It is an error which python throws during the execution of a program. When the error occurs, python creates an exception that can be handled which prevents our program from crashing.

**10. Unit test:-** 
It is the first level of software testing in python, in which the smallest testables part of software are tested. This helps in identifying that each unit of the software functions as designed.

**11. Constructor:-** 
Constructor is a unique kind of method that is called by python when it instantiates an object using the definitions in class.  

**12.Factory:-** 
It is  a creational design pattern used for creating implementations of a common interface. It helps in separating the procedure for creating an object using code that depends on the interface of the object. 

**13. Decorator:-** 
A decorator in python is a design pattern that permits the user to add new functionality to a current object without changing its structure. They are usually called before definition of a function we want to decorate.

**14. Extend class python:-**  
Extend allows one class to access and use the functions of the other class.

**15. CSV files:-**
A CSV file is a comma separated value, which is a file format  that are used for storing tabular data of excel or sheets.

**16. Reading files in Python:-**
Python allows us to Read,write and delete files. We can read files in python by using the "read" function to read the entire contents of a file.
