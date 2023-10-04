# Python

Introduction to Python

Python is a high-level, interpreted, interactive and object-oriented scripting language which finds its application in many areas like -

1.Webscripting

2.3D Modelling (Blender)

3. Desktop Applications: -`Games (Pygame)

4. Scientific usage (SciPy/NumPy)

Python source code is available under the GNU General Public License (GPL). There are two major Python versions, Python 2 and Python 3.


Python features:-

1. Open Source and Simple to use

2. Very powerful and Ubiquitous

3. Supports a broad standard library

4. Supports interactive testing and debugging

5. Established interface with all major DB's

6. Runs on variety of hardware platforms

![image](https://github.com/rukeshsungala/Python/assets/56673560/fe614f71-bae9-4801-adf1-4f809ec41c27)

Data types in Python:-

In this section, you will learn about the different Data types and pre-defined functions

1. int Type

2. float Type

3. Basic Math Functions

4. bool Type

Sequence types in Python:

In this section, you will learn about the different sequence types in Python and their applications.

1.str Type

2.bytes Type

3.bytearray Type

4.list Type 🔗https://www.youtube.com/watch?v=Eaz5e6M8tL4&ab_channel=Telusko

5.tuple Type 🔗https://www.youtube.com/watch?v=_GGaPgfynLo

6.Slicing  🔗https://youtu.be/ajrtAuDg3yw


Collection and Mapping types in Python
In this section, you will learn about the Collection and Mapping types in Python

1.range Type and Function 🔗https://youtu.be/0EqLWFKpQ1Q

2.set Type 🔗https://youtu.be/MEPlLAjPvXY

3.dict Type 🔗https://youtu.be/TxkMPxZgGho

Loops and Conditionals in Python
In this section, you will learn more about Loops and Conditionals in Python

1.While Loop 🔗https://youtu.be/D0Nb2Fs3Q8c

2.For Loop 🔗https://youtu.be/OnDr4J2UXSA

3.if Statement 🔗https://youtu.be/II5WTVvryvk


Introduction
Welcome to the world of Pythonista! Let's jump into course now. This course covers:

1.Functions

2.List Comprehensions

3. Iterators and Generators

4. Classes and Objects in Python

5. Closures and Decorators

6. Descriptors and Properties

1.Functions:-
A function is a piece of code capable of performing a similar task repeatedly.

It is defined using the def keyword in Python.


Syntax of a function:

     def <function_name>(<parameter1>, <parameter2>,...):
          'Function documentation'
          function_body
          return <value>         
 
Parameters, return expression, and documentation string are optional.

Sample function: square

     def square(x):
         'Returns square of a number.'
         return x**2

2.Common Built-in Functions

There are many built-in functions that Python offers. Here are some of them listed:

len: Returns the length of an object.

e.g : len('hello') = 5

type: Returns the type of an object.

e.g : type([2,3]) -> <type list>

range: Returns an iterator of a number sequence.

e.g : list(range(10, 13)) -> [10, 11, 12]

list(range(3)) -> [0, 1, 2]


3.Iterators

An Iterator is an object, which allows a programmer to traverse through all the elements of a collection, regardless of its specific implementation.

Values of an Iterator can be accessed only once and in sequential order.

Sample Iterator

     x = [6, 3, 1]
     s = iter(x)       
     print(next(s))      # -> 6
     print(next(s))      # -> 3
     print(next(s))      # -> 1
     print(next(s))      # -> StopIteration Error


4.List Comprehensions:-

Alternative to for loops.

More concise, readable, efficient and mimic functional programming style.

Used to:

Apply a method to all or specific elements of a list, and

Filter elements of a list satisfying specific criteria.

     Example
     x = [6, 3, 1]
     y = [ i**2 for i in x ]   # List Comprehension expression
     print(y)              # -> [36, 9, 1] 



5.Generators:
A Generator object is an iterator, whose values are created at the time of accessing them.

A generator can be obtained either from a generator expression or a generator function.

Example:

     x = [6, 3, 1]
     g = (i**2 for i in x) # generator expression
     print(next(g)) # -> 36
     
     def gen_number():  # generator function
         x = [6, 3, 1]
         for i in x:
             yield i**2
     x = gen_number()
     next(x)            # -> 36

Link to Watch for Iteratorsn and Generators:- https://youtu.be/zLqkC7COSCc


Introduction to OOP:-

Object-oriented programming can model real-life scenarios and suits developing large and complex applications.

Object:-

In real life, an object is something that you can sense and feel. For example Toys, Bicycles, Oranges and more.

However in Software development, an object is a non tangible entity, which holds some data and is capable of doing certain things.

Defining Classes:-

A Class is a template which contains,

-instructions to build an object.

-methods that can be used by the object to exhibit a specific behaviour.

class keyword is used to define a class in Python.

Syntax:

     class <ClassName>(<parent1>, ... ):
         class_body
         
Example

     class Person:
         pass
Above example defines Person class without any body.

Creating Objects:-

An object is created by calling the class name followed by a pair of parenthesis.

     class Person:             
         pass                    
     p1 = Person()      # Creating the object 'p1'
     print(p1)            # -> '<__main__.Person object at 0x0A...>'
     
The output of print on object p1, tell you what class it belongs to and hints on memory address it is referenced to.

Setting Attributes:-

You can set attributes, one a time, to an instantiated object and access it using the dot notation.

The value which is set to an attribute can be anything: a Python primitive, a built-in data type, another object. It can even be a function or a class.

Example

     class Person:
         pass
     p1 = Person()
     p1.fname = 'Jack'
     p1.lname = 'Simmons'
     print(p1.fname, '-', p1.lname)  # -> 'Jack - Simmons'

Setting Attributes Contd..

You can also set multiple attributes, at once, by defining the initializer method, __init__, inside the class.

This method is called by default, during an object creation.

It takes values passed inside the parenthesis, during an object creation, as it's arguments.

It also takes self as the first argument, which refers to the current object.

Setting Attributes Example:

In the following example, Person class sets two attributes using __init__ method.

     class Person:
         def __init__(self, fname, lname):
             self.fname = fname
             self.lname = lname
     p1 = Person('George', 'Smith')   
     print(p1.fname, '-', p1.lname)           # -> 'George - Smith'

Documenting a Class

Each class or a method definition can have an optional first line, known as docstring.

Example

     class Person:
         'Represents a person.'
         def __init__(self, fname, lname):
             'Initialises two attributes of a person.'
             self.fname = fname
             self.lname = lname

Understanding a Class

Once documented, you can load the script into an interactive interpreter and run help command on Person class.


     >>>help(Person)
     
     Help on class Person in module __main__:
     
     
     class Person(builtins.object)
     
      |  Represents a person.
     
      |  
     
      |  Methods defined here:
     
      |  
     
      |  __init__(self, fname, lname)
     
      |      Initialises two attributes of a person.
     
      |  
     
     ... and more


Inheritance:-

Inheritance describes is a kind of relationship between two or more classes, abstracting common details into super class and storing specific ones in the subclass.

To create a child class, specify the parent class name inside the pair of parenthesis, followed by it's name.

Example

     class Child(Parent):  
          pass
          
Every child class inherits all the behaviours exhibited by their parent class.

In Python, every class uses inheritance and is inherited from object by default.

Hence, the below two definitions of MySubClass are same.

Definition 1

     class MySubClass:   
        pass
        
Definition 2

     class MySubClass(object):   
         pass      
         
object is known as parent or super class.

MySubClass is known as child or subclass or derived class.

Inheritance in Action

     class Person:
         def __init__(self, fname, lname):
             self.fname = fname
             self.lname = lname
     class Employee(Person):
         all_employees = []
         def __init__(self, fname, lname, empid):
             Person.__init__(self, fname, lname)
             self.empid = empid
             Employee.all_employees.append(self)
             
Employee class is derived from Person.

     p1 = Person('George', 'smith')
     print(p1.fname, '-', p1.lname)
     e1 = Employee('Jack', 'simmons', 456342)
     e2 = Employee('John', 'williams', 123656)
     print(e1.fname, '-', e1.empid)
     print(e2.fname, '-', e2.empid)
     
Output

     George - smith
     Jack - 456342
     John - 123656
     
In the above example, Employee class utilizes __init __ method of the parent class Person to create its object.

Extending Built-in Types

Inheritance feature can be also used to extend the built-in classes like list or dict.

The following example extends list and creates EmployeesList, which can identify employees, having a given search word in their first name.

Example 1

     class EmployeesList(list):
         def search(self, name):
             matching_employees = []
             for employee in Employee.all_employees:
                 if name in employee.fname:
                     matching_employees.append(employee.fname)
             return matching_employees


Extending Built-in Types EmployeesList object can be used to store all employee objects, just by replacing statement all_employees = [] with all_employees = EmployeesList().

Example 2

     class Employee(Person):
         all_employees = EmployeesList()
         def __init__(self, fname, lname, empid):
             Person.__init__(self, fname, lname)
             self.empid = empid
             Employee.all_employees.append(self)
     
     e1 = Employee('Jack', 'simmons', 456342)
     e2 = Employee('George', 'Brown', 656721)
     print(Employee.all_employees.search('or'))
     
Output
     ​
     ['George']


Polymorphism:-

Polymorphism allows a subclass to override or change a specific behavior, exhibited by the parent class
​
Polymorphism Example

In the below shown example, you will find

Improvised Employee class with two methods getSalary and getBonus.

Definition of ContractEmployee class derived from Employee. It overrides functionality of getSalary and getBonus methods found in it's parent class Employee.

Example

     class Employee(Person):
         all_employees = EmployeesList ()
         def __init__(self, fname, lname, empid):
             Person.__init__(self, fname, lname)
             self.empid = empid
             Employee.all_employees.append(self)
         def getSalary(self):
             return 'You get Monthly salary.'
         def getBonus(self):
             return 'You are eligible for Bonus.'
     class ContractEmployee(Employee):
        def getSalary(self):
             return 'You will not get Salary from Organization.'
         def getBonus(self):
             return 'You are not eligible for Bonus.'
     e1 = Employee('Jack', 'simmons', 456342)
     e2 = ContractEmployee('John', 'williams', 123656)
     print(e1.getBonus())
     print(e2.getBonus())
     
Output

     You are eligible for Bonus.
     You are not eligible for Bonus.

Abstraction and Encapsulation:-

Abstraction means working with something you know how to use without knowing how it works internally.

Encapsulation allows binding data and associated methods together in a unit i.e class.

These principles together allows a programmer to define an interface for applications, i.e. to define all tasks the program is capable to execute and their respective input and output data.

A good example is a television set. We don’t need to know the inner workings of a TV, in order to use it. All we need to know is how to use the remote control (i.e the interface for the user to interact with the TV).

Abstracting Data

Direct access to data can be restricted by making required attributes or methods private, just by prefixing it's name with one or two underscores.

An attribute or a method starting with:

no underscores is a public one.

a single underscore is private, however, still accessible from outside.

double underscores is strongly private and not accessible from outside.

Abstraction and Encapsulation Example

empid attribute of Employee class is made private and is accessible outside the class only using the method getEmpid.

     class Employee(Person):
         all_employees = EmployeesList()
         def __init__(self, fname, lname, empid):
             Person.__init__(self, fname, lname)
             self.__empid = empid
             Employee.all_employees.append(self)
         def getEmpid(self):
             return self.__empid
          e1 = Employee('Jack', 'simmons', 456342)
     print(e1.fname, e1.lname)
     print(e1.getEmpid())
     print(e1.__empid)
     
Output

     Jack simmons
     456342
     AttributeError: Employee instance has no attribute '__empid'

Exceptions:

An exception is an error that occurs during execution of a program.

Python allows a programmer to handle such exceptions using try ... except clauses, thus avoiding the program to crash.

Some of the python expressions, though written correctly in syntax, result in error during execution. Such scenarios have to be handled.

Sample Exceptions

Try executing the following two expressions

10 + ( 1 / 0)

36 + '20'

The first one throws error message, ZeroDivisionError : division by zero, and

Second one throws, TypeError : unsupported operand type(s) for +: 'int' and 'str'.

In Python, every error message has two parts. The first part tells what type of exception it is and second part explains the details of error.

Handling Exception

Python handles exceptions using code written inside try ... except blocks.

A try block is followed by one or more except clauses.

The code to be handled is written inside try clause and the code to be executed when an exception occurs is written inside except clause.

Sample Exception Handling

Example 1

     try:
         a = pow(2, 4)
         print("Value of 'a' :", a)
         b = pow(2, 'hello')   # results in exception
         print("Value of 'b' :", b)
     except TypeError as e:
         print('oops!!!')
     print('Out of try ... except.')
     
Output

     Value of 'a' : 16
     oops!!!
     Out of try ... except.
     
You can observe from the output that execution of statements, present, after exception are skipped.

Raising Exceptions

raise keyword is used when a programmer wants a specific exception to occur.

Example 2

     try:
         a = 2; b = 'hello'
         if not (isinstance(a, int)
                 and isinstance(b, int)):
             raise TypeError('Two inputs must be integers.')
         c = a**b
     except TypeError as e:
         print(e)
         
Output

     Two inputs must be integers.
     
Above example raises TypeError when either a or b are not integers.

User Defined Functions

There are many built-in exceptions in Python, which are directly or indirectly derived from Exception class.

Python also allows a programmer to create custom exceptions, derived from base Exception class.

Example 1

     class CustomError(Exception):
         def __init__(self, value):
             self.value = value
         def __str__(self):
             return str(self.value)
     try:
          a = 2; b = 'hello'
         if not (isinstance(a, int) and isinstance(b, int)):    
                 raise CustomError('Two inputs must be integers.')
           c = a**b
     except CustomError as e:
          print(e)
    
Output

     Two inputs must be integers.
     
CustomError is raised in above example, instead of TypeError.

Using 'finally' clause

finally clause is an optional one that can be used with try ... except clauses.

All the statements under finally clause are executed irrespective of exception occurrence.

Example 1

     def divide(a,b):
         try:
             result = a / b
             return result
         except ZeroDivisionError:
             print("Dividing by Zero.")
         finally:
             print("In finally clause.")
     print('First call')
     print(divide(14, 7))
     print('Second call')
     print(divide(14, 0))

Output

     First call
     In finally clause.
     2.0
     Second call
     Dividing by Zero.
     In finally clause.
     None
     
Statements inside finally clause are executed in both function calls.

Using 'else' clause

else clause is also an optional clause with try ... except clauses.

Statements under else clause are executed only when no exception occurs in try clause.

Example 2

     try:
         a = 14 / 7
     except ZeroDivisionError:
         print('oops!!!')
     else:
         print('First ELSE')
     try:
         a = 14 / 0
     except ZeroDivisionError:
         print('oops!!!')
     else:
         print('Second ELSE')
         
Output

     First ELSE
     oops!!!


Introduction to a Module:

Any file containing logically organized Python code can be used as a module.

A module generally contains any of the defined functions, classes and variables. A module can also include executable code.

Any Python source file can be used as a module by using an import statement in some other Python source file.

Packages:🔗https://youtu.be/urE5MuYd-YM

A package is a collection of modules present in a folder. The name of the package is the name of the folder itself. A package generally contains an empty file named __init__.py in the same folder, which is required to treat the folder as a package. Know more on importing utilities of a module or a package, from the below video.
