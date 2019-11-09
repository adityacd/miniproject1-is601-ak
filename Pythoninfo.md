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
```
class MyWSD:
  x = 7

k1 = MyWSD()     #defined object
print(k1.x)
```

**6. Static:-** 
A static is a method which is bound to a class, rather than the objects for that class. It can be called without an object.
```
class Calculator:

    def multiplyNums(x, y):
        return x + y

# create addNumbers static method
Calculator.multiplyNums = staticmethod(Calculator.multiplyNums)

print('Product:', Calculator.multiplyNums(15, 110))
```

**7. Property/Attribute:-** 
An attribute belongs to a class itself and it is shared by all instances of that class, it is defined in the class body at the top. Instance attributes are not are not shared by objects.
```
class Student:
    def __init__(self, name, marks):
        self.name = name
        self.marks = marks
        # self.gotmarks = self.name + ' obtained ' + self.marks + ' marks'

    @property
    def gotmarks(self):
        return self.name + ' obtained ' + self.marks + ' marks'

    @gotmarks.setter
    def gotmarks(self, sentence):
        name, rand, marks = sentence.split(' ')
        self.name = name
        self.marks = marks


st = Student("Jaki", "25")
print(st.name)
print(st.marks)
print(st.gotmarks)
print("##################")
st.name = "Anusha"
print(st.name)
print(st.gotmarks)
print("##################")
st.gotmarks = 'Golam obtained 36'
print(st.gotmarks)
print(st.name)
print(st.marks)
```

**8. Method:-** 
Method is a function that is available for an object due to the object’s type and it is a member of the class.
```
# Python 3  User-Defined  Method 
class ABC : 
    def method_abc (self): 
        print("I am in method_abc of ABC class. ") 
  
class_ref = ABC() # object of ABC class 
class_ref.method_abc() 
```

**9. Exception:-**
It is an error which python throws during the execution of a program. When the error occurs, python creates an exception that can be handled which prevents our program from crashing.
```
>>> 10 * (1/0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
>>> 4 + spam*3
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'spam' is not defined
>>> '2' + 2
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: Can't convert 'int' object to str implicitly
```

**10. Unit test:-** 
It is the first level of software testing in python, in which the smallest testables part of software are tested. This helps in identifying that each unit of the software functions as designed.
```
import unittest

class TestStringMethods(unittest.TestCase):

    def test_upper(self):
        self.assertEqual('foo'.upper(), 'FOO')

    def test_isupper(self):
        self.assertTrue('FOO'.isupper())
        self.assertFalse('Foo'.isupper())

    def test_split(self):
        s = 'hello world'
        self.assertEqual(s.split(), ['hello', 'world'])
        # check that s.split fails when the separator is not a string
        with self.assertRaises(TypeError):
            s.split(2)

if __name__ == '__main__':
    unittest.main()
  ```
**11. Constructor:-** 
Constructor is a unique kind of method that is called by python when it instantiates an object using the definitions in class.  
```

class karankaul: 
    karan = "" 
  
    # default constructor 
    def __init__(self): 
        self.karan = "karankaul"
  
    # a method for printing data members 
    def print_karan(self): 
        print(self.karan) 
  
  
# creating object of the class 
obj = karankaul() 
  
# calling the instance method using the object obj 
obj.print_karan() 
```

**12.Factory:-** 
It is  a creational design pattern used for creating implementations of a common interface. It helps in separating the procedure for creating an object using code that depends on the interface of the object. 
```
class SongSerializer:
    def serialize(self, song, format):
        serializer = self._get_serializer(format)
        return serializer(song)

    def _get_serializer(self, format):
        if format == 'JSON':
            return self._serialize_to_json
        elif format == 'XML':
            return self._serialize_to_xml
        else:
            raise ValueError(format)

    def _serialize_to_json(self, song):
        payload = {
            'id': song.song_id,
            'title': song.title,
            'artist': song.artist
        }
        return json.dumps(payload)

    def _serialize_to_xml(self, song):
        song_element = et.Element('song', attrib={'id': song.song_id})
        title = et.SubElement(song_element, 'title')
        title.text = song.title
        artist = et.SubElement(song_element, 'artist')
        artist.text = song.artist
        return et.tostring(song_element, encoding='unicode')
```
**13. Decorator:-** 
A decorator in python is a design pattern that permits the user to add new functionality to a current object without changing its structure. They are usually called before definition of a function we want to decorate.
```
# defining a decorator 
def hello_decorator(func): 
  
    # inner1 is a Wrapper function in  
    # which the argument is called 
      
    # inner function can access the outer local 
    # functions like in this case "func" 
    def inner1(): 
        print("Hello, this is before function execution") 
  
        # calling the actual function now 
        # inside the wrapper function. 
        func() 
  
        print("This is after function execution") 
          
    return inner1 
  
  
# defining a function, to be called inside wrapper 
def function_to_be_used(): 
    print("This is inside the function !!") 
  
  
# passing 'function_to_be_used' inside the 
# decorator to control its behavior 
function_to_be_used = hello_decorator(function_to_be_used) 
  
  
# calling the function 
function_to_be_used() 
```

**14. Extend class python:-**  
Extend allows one class to access and use the functions of the other class.

**15. CSV files:-**
A CSV file is a comma separated value, which is a file format  that are used for storing tabular data of excel or sheets.
```
import csv

with open('employee_birthday.txt', mode='r') as csv_file:
    csv_reader = csv.DictReader(csv_file)
    line_count = 0
    for row in csv_reader:
        if line_count == 0:
            print(f'Column names are {", ".join(row)}')
            line_count += 1
        print(f'\t{row["name"]} works in the {row["department"]} department, and was born in {row["birthday month"]}.')
        line_count += 1
    print(f'Processed {line_count} lines.')
```
**16. Reading files in Python:-**
Python allows us to Read,write and delete files. We can read files in python by using the "read" function to read the entire contents of a file.
