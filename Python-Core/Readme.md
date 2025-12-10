# Table of Contents

- [01 Setup](#01-setup)
  - [Main](#main)
- [02 Python Syntax](#02-python-syntax)
  - [Main](#main)
- [03 Variables](#03-variables)
  - [01 Basics](#01-basics)
  - [02 Data Types](#02-data-types)
- [04 Typecasting](#04-typecasting)
  - [01 Typecasting](#01-typecasting)
  - [02 Example](#02-example)
- [05 User Input](#05-user-input)
  - [01 Input](#01-input)
  - [02 Add](#02-add)
- [06 Comments Print Esc](#06-comments-print-esc)
  - [01 Comments](#01-comments)
  - [02 Escape](#02-escape)
  - [03 Print](#03-print)
- [07 Operators](#07-operators)
  - [01 Arithmetic Operators](#01-arithmetic-operators)
  - [02 Conditional Operators](#02-conditional-operators)
  - [03 Logical Operators](#03-logical-operators)
  - [04 Assignment Operators](#04-assignment-operators)
- [08 Conditionals](#08-conditionals)
  - [01 If Statement](#01-if-statement)
  - [02 If Else](#02-if-else)
  - [03 If Elif Else](#03-if-elif-else)
  - [04 Match Case](#04-match-case)
- [09 Loops](#09-loops)
  - [01 For Loops](#01-for-loops)
  - [02 While Loop](#02-while-loop)
  - [03 Infinite Loops](#03-infinite-loops)
  - [04 Break](#04-break)
  - [05 Continue](#05-continue)
  - [06 Pass](#06-pass)
- [10 Strings.Py](#10-strings.py)
  - [01 String](#01-string)
  - [02 Indexing](#02-indexing)
  - [03 Slicing](#03-slicing)
  - [04 String Methods](#04-string-methods)
  - [05 Fstrings](#05-fstrings)
- [11 Functions](#11-functions)
  - [01 Functions](#01-functions)
  - [02 Function Arguments](#02-function-arguments)
  - [03 Lambda](#03-lambda)
  - [04 Recursion](#04-recursion)
  - [05 Modules](#05-modules)
  - [06 Function Scope](#06-function-scope)
  - [07 Global](#07-global)
  - [08 Docstrings](#08-docstrings)
  - [Mymodule](#mymodule)
- [12 Lists](#12-lists)
  - [01 Lists](#01-lists)
  - [02 List Methods](#02-list-methods)
  - [03 List Comprehension](#03-list-comprehension)
- [13 Tuples](#13-tuples)
  - [01 Tuples](#01-tuples)
  - [02 Tuple Unpacking](#02-tuple-unpacking)
  - [03 Tuple Methods](#03-tuple-methods)
- [14 Sets](#14-sets)
  - [01 Sets](#01-sets)
  - [02 Set Methods](#02-set-methods)
  - [03 Set Operation](#03-set-operation)
- [15 Dictionaries](#15-dictionaries)
  - [01 Dictionary](#01-dictionary)
  - [02 Dict Methods](#02-dict-methods)
  - [03 Dict Comprehensions](#03-dict-comprehensions)
- [16 Oops](#16-oops)
  - [01 Class](#01-class)
  - [02 Constructors](#02-constructors)
  - [03 Instance Class](#03-instance-class)
  - [04 Inheritance](#04-inheritance)
  - [05 Operator Overloading](#05-operator-overloading)
- [17 Python Advanced Concepts](#17-python-advanced-concepts)
  - [01 Decorators](#01-decorators)
  - [02 Dec With Args](#02-dec-with-args)
  - [03 Getter And Setters](#03-getter-and-setters)
  - [04 Instance Static Class](#04-instance-static-class)
  - [05 Dunder](#05-dunder)
  - [06 Errors](#06-errors)
  - [07 Else](#07-else)
  - [08 Finally](#08-finally)
  - [09 Map](#09-map)
  - [10 Filter](#10-filter)
  - [11 Reduce](#11-reduce)
  - [12 Walrus](#12-walrus)
  - [13 Args](#13-args)
  - [14 Kwargs](#14-kwargs)
  - [15 Combined Args Kwargs](#15-combined-args-kwargs)
- [18 Files](#18-files)
  - [01 Read](#01-read)
  - [02 Write](#02-write)
  - [03 Append](#03-append)
  - [04 Line By Line](#04-line-by-line)
  - [05 With](#05-with)
  - [06 Os](#06-os)
  - [07 Shutil](#07-shutil)
  - [08 Argparse](#08-argparse)
  - [John Doe](#john-doe)
  - [Harry](#harry)
- [19 External Modules](#19-external-modules)
  - [01 Venv](#01-venv)
  - [02 Requests](#02-requests)
  - [03 Regular Ex](#03-regular-ex)
  - [04 Threading](#04-threading)
  - [Codewithharry](#codewithharry)
  - [Requirements](#requirements)
- [20 Ai](#20-ai)
  - [01 String Function](#01-string-function)
  - [02 Tic Tac Toe](#02-tic-tac-toe)
  - [03 Llm Api](#03-llm-api)
- [21 Projects](#21-projects)

---

# 01 Setup

## Main

```python
print("Hello World")
```

# 02 Python Syntax

## Main

```python
print("Hello Harry")
print("I am good")
print("How are you?")
print(3)

# if(a>3):
#     statement1
#     statement3
# statement2
```

# 03 Variables

## 01 Basics

```python
# In Python, variables are used to store data that can be used and manipulated throughout a program. A variable is created the moment you assign a value to it using the assignment operator (=).

age = 34 # integer
name = "Harry" # string
cgpa = 4.55 # float

# Rule of defining a variable in Python  
# Variable names must start with a letter (a-z, A-Z) or an underscore (_).
# They can contain letters, numbers, and underscores.
# Variable names are case-sensitive (age and Age are different).
# Avoid using Python keywords (e.g., if, for, while) as variable names.

# 34age = 4 # Invalid because variable cannot start with a number
age = 32 # Valid because variable can start with a number 
# a$$ge = 45 # Invlaid because variables cannot contain special characters other than _
__age = 34
__nice_45 = 34
a_b_c_7 = "Sam"
```

## 02 Data Types

```python
# Python supports several built-in data types:
#     Integers (int): Whole numbers (e.g., 10, -5).
#     Floats (float): Decimal numbers (e.g., 3.14, -0.001).
#     Strings (str): Text data enclosed in quotes (e.g., "Hello", 'Python').
#     Booleans (bool): Represents True or False.
#     Lists: Ordered, mutable collections (e.g., [1, 2, 3]).
#     Tuples: Ordered, immutable collections (e.g., (1, 2, 3)).
#     Sets: Unordered collections of unique elements (e.g., {1, 2, 3}).
#     Dictionaries: Key-value pairs (e.g., {"name": "Alice", "age": 25}).

age = 3 
print(age)
print(type(age))

cgpa = 8.2
print(cgpa)
print(type(cgpa))

name = "Harry"
print(name)
print(type(name))

is_completed = True # can also be False
print(is_completed)
print(type(is_completed))
```

# 04 Typecasting

## 01 Typecasting

```python
a = 34 
b = "34"
d = 223


print(a)
print(type(a))

print(b)
print(type(b))

# Convert b to an integer
c = int(b)
print(c)
print(type(c))

e = str(d)
print(e)
print(type(e))
```

## 02 Example

```python
# Convert string to integer
num_str = "10"
num_int = int(num_str)
print(num_int) # Output: 10
print(type(num_int))

# Convert integer to string
num = 25
num_str = str(num)
print(num_str) # Output: "25"
print(type(num_str))

# Convert float to integer
pi = 3.14
pi_int = int(pi)
print(pi_int) # Output: 3
print(type(pi_int))
```

# 05 User Input

## 01 Input

```python
a = input("Enter a number")
print(a)

b = input("Enter your name: ")
print(b)
```

## 02 Add

```python
# a = input("Enter first number") 
# a = int(a) # convert a to int version of a
# print(a + 3)

a = int(input("Enter first number"))
# a = int(a)
b = int(input("Enter second number"))
# b = int(b)

print(a + b)
```

# 06 Comments Print Esc

## 01 Comments

```python
print("Hey how are you?")

# Arjun please finish this code 


# Rohan, please review what arjun has done
'''
mments are used to explain code and are ignored by the Python
interpreter.
Single-line comments start with # .
Multi-line comments are enclosed in  or """ .
Escape Sequences
Escape sequences are used to include special characters in strings.
Common escape sequences:
\n : Newline
\t : Tab
\\ : Backslash
\" : Double quote
\' : Single quote
Example:
Print Statement
The print() function is used to display output.
•
•
•
# This is a single
'''
```

## 02 Escape

```python
print("Hey how are you\nI am good\\newline")

print("Hello \" World")
```

## 03 Print

```python
# print('Hello World',"Harry",5, sep="/")
print('Hello World', end="..")
print('Harry', end="//")
```

# 07 Operators

## 01 Arithmetic Operators

```python
a = 34

b = 2 

# Arithmetic Operator 
print("a + b = ", a + b)
print("a - b = ", a - b)
print("a * b = ", a * b)
print("a / b = ", a / b)
print("a % b = ", a % b)
print("a // b = ", a // b)
print("a ** b = ", a ** b)
 
```

## 02 Conditional Operators

```python
a = 34

b = 2

# Conditional Operators 
print(a>4)
print(a<4)
print(a<=4)
print(a>=4)
print(a==4) # Is a equal to 4?
print(a==34) # Is a equal to 34?
print(a!=34) # Is a not equal to 34?
```

## 03 Logical Operators

```python
c = True 
d = False

# Logical Operators
print(True and True)
print(True and False)
print(False and True)
print(False and False)

print("For Or Operator...")
print(True or True)
print(True or False)
print(False or True)
print(False or False)

print("Not Operator")
print(not(True) ) 
print(not(False) ) 
```

## 04 Assignment Operators

```python
a = 32
print(a)
a*=3
print(a)
```

# 08 Conditionals

## 01 If Statement

```python
age = 12

if(age>18):
    print("You can drive")
    print("Thank you ")

print("End of program")
```

## 02 If Else

```python
age = int(input("Enter your age: "))

if(age>18):
    print("You can drive")
else:
    print("You cannot drive")

print("End of program")
```

## 03 If Elif Else

```python
age = int(input("Enter your age: "))

if(age>18):
    print("You can drive")
elif(age == 18):
    print("Lets schedule an interview")
elif(age == 0):
    print("Hey you are just born")
else:
    print("Sorry you cannot drive")
```

## 04 Match Case

```python
a = int(input("Enter a number between 1 and 10: "))

match a:
    case 1:
        print("You won a charger")
    case 3:
        print("You won $3")
    case 6:
        print("You won a camera")
    case _:
        print("Better luck next time")
    

```

# 09 Loops

## 01 For Loops

```python
# print(1)
# print(2)
# print(3)
# print(4)
# print(5)

# for i in range(1, 6): # range function goes from 1 to (6-1) ie 5 in this case
#     print(i)

for i in range(1, 11):
    print("5 X", i, "=",  5*i)
```

## 02 While Loop

```python
# print(1)
# print(2)
# print(3)
# print(4)
# print(5)

i = 1
while i<6:
    print(i)
    i = i + 1
```

## 03 Infinite Loops

```python
i = 1
while True:
    print(i)
    i = i + 1 
```

## 04 Break

```python
for i in range(0, 21):
    print(i)
    if i == 11:
        break # Cancel the execution of this loop now
```

## 05 Continue

```python
for i in range(1, 20):
    if i == 10:
        continue # continue the loop for the next iteration here itself
    print(i)

    
```

## 06 Pass

```python
i = 3

if i == 32:
    pass # do nothing
print("End of program")
```

# 10 Strings.Py

## 01 String

```python
# name = "Harry"
name = 'Harry'
# name = '''Harry is a good boy'''
print(name)
```

## 02 Indexing

```python
name = "Harry" 

# name = "H   a   r  r   y"
#         0   1   2  3   4
#        -5  -4  -3 -2  -1

# print(name[0])
# print(name[1])
# print(name[2])
# print(name[3])
# print(name[4])
# print(name[5])

print(name[-1])
print(name[-2])
print(name[-3])
print(name[-4]) # name[-4+5] name[1]
print(name[-5])
```

## 03 Slicing

```python
name = "Harry0123456789"

# print(name[0:2]) # goes from 0 to 2-1 ie 0 to 1

# print(name[2:-1]) # Same as name[2:4]

# print(name[0:10:n]) # Skip n- 1 characters
print(name[0:10:1]) # Skip 0 character
print(name[0:10:3]) # Skip 3-1 ie 2 characters

print(name[:4]) # Replace the first empty number with 0 # name[0:4]
print(name[1:]) # Replace the second empty number with length # name[1:15]
```

## 04 String Methods

```python
s = "hello world" # Strings are immutable

# s[0] = "R" # You cannot do this

a = len(s)
# print(a)
# print(s.upper(), s)
# print(s.lower())
# print(s.capitalize())
# print(s.title())

# text = " \nhello world "
# print(text.strip()) # Output: "hello world"
# print(text.lstrip()) # Output: "hello world "
# print(text.rstrip()) # Output: " hello world"


# text = "Python is fun and fun and fun"
# print(text.find("is")) # Output: 7 Index of first occurence
# print(text.replace("fun", "awesome")) 


# text = "Apples,Bananas,Pineapples"
# print(text.split(","))
# print(",".join(['Apples', 'Bananas', 'Pineapples']))

text = "Python123"
print(text.isalpha()) # Output: False
print(text.isdigit()) # Output: False
print(text.isalnum()) # Output: True
print(text.isspace()) # Output: False
```

## 05 Fstrings

```python
# String formatting

template = "Dear {}, You are awesome. Take this {}$ bag"
a = "John"
a1 = 10000
b = "Jack"
b1 = 1000
c = "Marie"
c2 = 300

s1 = template.format(a, a1)
print(s1)

print(f"{a} you are awesome and take this {a1}$ bag")
```

# 11 Functions

## 01 Functions

```python
# a = 4
# b = 2
# c = 1

# average = (a + b + c)/3.0
# print(average)

# a1 = 6
# b1 = 7
# c1 = 12

# average1 = (a1 + b1 + c1)/3
# print(average1)


def average(a, b, c):
    d = (a + b + c)/3.0
    # print(d)
    return d

o1 = average(3, 5, 1)
o2 = average(4, 2, 1)

print(o1)
print(o2)
```

## 02 Function Arguments

```python
def add(a, b, plus=0):
    x = a + b + plus
    return x


c = add(3, 5, 2)
print(c)

c1 = add(b=5, a=3)
```

## 03 Lambda

```python
square = lambda x: x*x 
'''
As good as writing
def square(x):
    return x*x
'''
sum = lambda x, y: x+y
'''
As good as writing
def sum(x, y):
    return x + y
'''

print(square(3))
print(sum(3, 62))
```

## 04 Recursion

```python
''' 
0 1 1 2 3 5 8 13
0 1 2 3 4 5 6.....

fib(0) = 0
fib(1) = 1
fib(2) = fib(0) + fib(1)
fib(3) = fib(1) + fib(2)
fib(4) = fib(2) + fib(3)
fib(n) = fib(n-2) + fib(n-1)

'''

def fib(n):
    # Base case of recursion
    if(n == 0 or n == 1):
        return n

    return fib(n-2) + fib(n-1)

print(fib(6))

fib(4) + fib(5)
fib(2) + fib(3) + fib(5)
fib(0) + fib(1) + fib(3) + fib(5)
0 + 1 + fib(1) + fib(2) + fib(3) + fib(4)
0 + 1 + 1 + fib(0) + fib(1) + fib(1) + fib(2)+ fib(4)
0 + 1 + 1 + 0 + 1 + 1 + fib(0) + fib(1) + fib(2) + fib(3)
0 + 1 + 1 + 0 + 1 + 1 + 0 + 1 + fib(0) + fib(1) + fib(3)
0 + 1 + 1 + 0 + 1 + 1 + 0 + 1 + 0 + 1 + fib(1) + fib(2)
0 + 1 + 1 + 0 + 1 + 1 + 0 + 1 + 0 + 1 + 1 + fib(0) + fib(1)
0 + 1 + 1 + 0 + 1 + 1 + 0 + 1 + 0 + 1 + 1 + 0 + 1
```

## 05 Modules

```python
# Two types of modules in Python: 
# - Built in Modules 
# - External Modules
# List of all the built in Modules: https://docs.python.org/3/py-modindex.html
import math 
import os 
import mymodule
import requests

print(math.sqrt(16))
mymodule.hello()
r = requests.get("https://www.google.com")
print(r.text)
```

## 06 Function Scope

```python
def sum(a, b):
    # a and b are local variables
    c = a + b 
    z = 1 # It creates a local variable called z which is destroyed after this function returns
    return c

def greet():
    z = 32 # Local variable
    print("Hello")
    
z = 8 # z is a global variable
print(z)
print(sum(4, 6)) 
print(z)
```

## 07 Global

```python
def sum(a, b):
    print("Hey I am summing ")
    c = a + b
    global z # Please modify global z
    z = 0 # This will refer to global z and not create a local variable
    return c 

z = 3
print(sum(3, 12))
print(z)
```

## 08 Docstrings

```python
def sum(a, b): 
    '''This will sum two numbers'''
    c = a + b  
    return c

print(sum.__doc__)
```

## Mymodule

```python
def hello():
    print("Hello world")
```

# 12 Lists

## 01 Lists

```python
marks = [54, 23, 64, 93, 32]
mixed = [43, "Hello", False, 4.2]

print(marks[2:4])
print(marks[2])
print(mixed[4]) # Error Index out of bound
```

## 02 List Methods

```python
marks = [5, 2, 21, 5, 7]
extra_marks = [53, 23, 32]

print(marks)
# marks.append(63) # This will change the original list
# marks.pop()
marks.extend(extra_marks)
print(marks)
```

## 03 List Comprehension

```python
# Create a list containing the table of 5


# table = []

# for i in range(1, 11):
#     table.append(5*i)

table = [5*i for i in range(1, 11)]

print(table)
```

# 13 Tuples

## 01 Tuples

```python
a = (3, 2, 22, 13)

print(a)
print(a[2])
a[3] = 32

b = (3, )
```

## 02 Tuple Unpacking

```python
tu = (3, 2, 45)

a, b, c = tu 

print(a, b, c)
```

## 03 Tuple Methods

```python
t = (3, 12, 1, 54, 23, 12)

print(t.count(12))
print(t.index(12))
```

# 14 Sets

## 01 Sets

```python
s = {3, 23, 2, 11}

print(s, type(s))
# print(s[3]) # You are not allowed to do something like this
```

## 02 Set Methods

```python
s = {34, 23, 1, 3, 22}

print(s)

s.add(32)
s.add(322)
s.remove(1)
# s.remove(434234) # Throws an error
s.discard(42323)
print(s)
```

## 03 Set Operation

```python
a = {3, 23, 1}
b = {23, 4, 2, 55, 1}

c = a.union(b) # Contains all the elements in a along with all the elements in b
print(c)

d = a.intersection(b) # Contains only the elements that are present in a as well as b
print(d)

```

# 15 Dictionaries

## 01 Dictionary

```python
marks = {"harry": 34, "jack": 45, "lily": 94 }

# print(marks, type(marks))
print(marks["lily"])
marks["harry"] = 3
print(marks)
```

## 02 Dict Methods

```python
marks = {"harry": 34, "jack": 45, "lily": 94 }

print(marks.keys())
print(marks.values())
# marks.clear()
marks.pop("lily")
print(marks)

```

## 03 Dict Comprehensions

```python
table_of_5 = {i: 5*i for i in range(1, 11)}

print(table_of_5)
```

# 16 Oops

## 01 Class

```python
# Class: Class is a blueprint or a template. Eg. Form for an Exam that contains name, age, electives, father's name etc

# Object: Specific instance created from the template (class.). Eg. Form which contains the data for John Doe

class Employee:
    company = "HP"

    def get_salary(self): # self is important here because self is a way to reference the object of the class which is being created
        return 34000


e1 = Employee() # An Object of class Employee is created here
print(e1.get_salary()) # Employee e's get salary method is called

e2 = Employee()
print(e2.get_salary())
print(e2.company)
```

## 02 Constructors

```python
class Employee: 

    def __init__(self, salary, name, bond):
        self.salary = salary # Create an instance attribute of name salary and assign it with salary
        self.name = name 
        self.bond = bond

    def get_salary(self):
        return self.salary

    def get_info(self):
        print(f"The name of the employee is {self.name}. Salary is {self.salary}. The bond is for {self.bond} years")
    

e1 = Employee(34000, "John Doe", 4)
# print(e1.get_salary())
e1.get_info()
```

## 03 Instance Class

```python
class Employee: 
    company = "Asus" # This is class attribute

    def __init__(self, salary, name, bond, company):
        self.salary = salary # Create an instance attribute of name salary and assign it with salary
        self.name = name 
        self.bond = bond
        self.company = company

    def get_salary(self):
        return self.salary

    def get_info(self):
        print(f"The name of the employee is {self.name}. Salary is {self.salary}. The bond is for {self.bond} years")


e1 = Employee(3400, "John", 3, "Tesla")
print(e1.company) # will always print instance attribute whenever present
print(Employee.company) # This will always print the class attribute

# Object introspection 
print(dir(e1))
```

## 04 Inheritance

```python
class Animal: # Parent class (superclass)
    location = "Australia"
    def __init__(self, name):
        self.name = name
    def speak(self):
        print("Speaking now....")

class Dog(Animal): # This is how inheritance is done in Python
    def speak(self):
        super().speak() # We are using the speak function of the parent class
        print("Woof!")

# a = Animal("Dog")
# a.speak()
d = Dog("Bruno")
d.speak()
# print(d.location)
```

## 05 Operator Overloading

```python
class Point:
    def __init__(self, x, y):
        self.x = x 
        self.y = y

    def sum(self, p):
        return Point((self.x + p.x), (self.y + p.y))
    
    def print_point(self):
        print(f"X is {self.x} and Y is {self.y}")

    def __add__(self, p):
        return Point((self.x + p.x), (self.y + p.y))

p1 = Point(3, 2)
p2 = Point(6, 3)

# p = p1.sum(p2) # Returns a new point which is sum of p1 and p2
p = p1 + p2 # We overloaded the + Operator by writing __add__ function
p.print_point()
```

# 17 Python Advanced Concepts

## 01 Decorators

```python
# Decorator is a function that takes a function, it creates a new function inside its body (wrapper). Then it returns that new function
def decorator(func):
    def wrapper():
        print("I am about to execute a function....")
        func()
        print("I have executed this function....")
    return wrapper

@decorator
def say_hello():
    print("Hello!")

say_hello()
# f = decorator(say_hello)
# f()

'''
f will look something like this
def f():
    print("I am about to execute a function....")
    print("Hello!")
    print("I have executed this function....")
'''

```

## 02 Dec With Args

```python
def repeat(n):
    def decorator(func):
        def wrapper(a):
            for i in range(n):
                func(a)
        return wrapper 
    return decorator

@repeat(7)
def say_hello(a):
    print(f"Hello! {a}")

'''
It replaces the function say_hello with this:
def decorator(func):
    def wrapper(a):
        for i in range(n):
            say_hello(a)
    return wrapper
'''

say_hello("Harry")
```

## 03 Getter And Setters

```python
class Employee:
    def __init__(self, name, salary):
        self.name = name 
        self.salary = salary

    @property
    def first_name(self):
        l = self.name.split(" ") 
        return l[0]
    
    @first_name.setter
    def first_name(self, first):
        l = self.name.split(" ")
        new_name = f"{first} {l[1]}" 
        self.name = new_name

e = Employee("Jack Doe", 34555)
# print(e.first_name())
# e.set_first_name("John")
# print(e.name)

print(e.first_name)
e.first_name = "John"
print(e.name)
```

## 04 Instance Static Class

```python
class Employee:
    company = "HP"
    def __init__(self, name, salary):
        self.name = name 
        self.salary = salary

    # Instance method (default)
    def print_info(self):
        info = f"The name is {self.name} and the salary is {self.salary}"
        print(info)

    # Static Method    
    @staticmethod
    def sum(a, b):
        return a+b
    
    # Class Methods 
    @classmethod
    def print_company(cls):
        print(cls.company)

    @classmethod
    def change_company(cls, new_company):
        cls.company = new_company



e1 = Employee("Jack", 3455)
e2 = Employee("Jill", 34355)
# print(Employee.company)
# print(Employee.name) # this will throw an error
# e1.print_info()
# e2.print_info()

# print(e2.sum(5, 23))
print(Employee.company)
e1.change_company("Acer")
print(Employee.company)
```

## 05 Dunder

```python
class Employee:
    company = "HP"
    def __init__(self, name, salary):
        self.name = name 
        self.salary = salary

    def __str__(self):
        return f"The name is {self.name} and the salary is {self.salary}"
    
    def __repr__(self):
        return f"name: {self.name}\nsalary: {self.salary}"
    
    def __len__(self):
        return len(self.name)


e = Employee("Harry", 43566)
print(len(e))
# print(e.name, e.salary)
# print(str(e))
# print(repr(e))
```

## 06 Errors

```python
# while True:
#     try: 
#         a = int(input("Enter number 1: "))
#         b = int(input("Enter number 2: "))
#         print(f"The division is {a / b}")

#     except ValueError:
#         print("Please dont perform bad typecasts")
    
#     except ZeroDivisionError:
#         print("Hey dont divide by 0")

#     except Exception as e:
#         print("Unknown error occurred!", e)

a = int(input("Enter number 1: "))
b = int(input("Enter number 2: "))

if b == 0:
    raise ValueError("Please dont divide by 0")

print(f"The division is {a / b}")
```

## 07 Else

```python
try:
    a = 345/10

except Exception as e:
    print(e)

# Gets executed when there is no error in the try block 
else:
    print("Hey I am good")




```

## 08 Finally

```python
def divide(a, b):
    try:
        c = a/b 
        print(c)
        return c

    except Exception as e:
        print(e)
        return None

    # This is always executed no matter if try completely executes or not 
    finally: 
        print("This is always executed")

a = int(input("Enter number 1: "))
b = int(input("Enter number 2: "))
divide(a, b)
```

## 09 Map

```python
numbers = [1, 2, 3, 45, 4, 21]

# def square(x):
#     return x * x 


new = list(map(lambda x: x*x, numbers))
print(new)
```

## 10 Filter

```python
# def is_greater_than_9(x):
#     if x>9:
#         return True
#     else:
#         return False
    
a = [1, 3, 5, 234, 34, 32, 6543, 23, 2 ,5 , 6, 7 ,43]

new = list(filter(lambda x: x>9, a))
print(new)
```

## 11 Reduce

```python
from functools import reduce

numbers = [1, 2, 3, 4, 5, 6]
#         [3, 3, 4, 5, 6]
#         [6, 4, 5, 6]
#         [10, 5, 6]
#         [15, 6]
#         [21]

def sum(a, b):
    return a + b 

c = reduce(sum, numbers)
print(c)
```

## 12 Walrus

```python
def very_slow_func():
    print("Something....")
    print("Something....")
    print("Something....")
    print("Something....")
    print("Something....")
    return 70

# # a = very_slow_func()
# if((a:=very_slow_func())>10):
#     print(a)

# else:
#     print("Its not greater than 10")

while(data:=input("Enter the value: ")):
    print(data)
    if data == "q":
        break 
```

## 13 Args

```python
def sum(*args): 
    # args will be a tuple of all the values passed to sum 
    total = 0
    for item in args:
        total += item 
    return total


print(sum(342, 2, 7, 9))
```

## 14 Kwargs

```python
def marks(**kwargs):
    # kwargs is a dictionary with all the key value pairs which were passed to marks 
    for item in kwargs.keys():
        print(f"The marks of {item} is {kwargs[item]}")

marks(shubham=34, vikrant=54, jack=34, Marie=90, Priya=45)
```

## 15 Combined Args Kwargs

```python
def func1(*args, **kwargs):
    print(args)
    print(kwargs)

func1(1, 2, 4, 5, jack=34, jill=32, marie=31)
```

# 18 Files

## 01 Read

```python
f = open("harry.txt", "r")

content = f.read()

print(content)

f.close()
```

## 02 Write

```python
# Write to a file called John Doe.txt 
# It should contain data about John Doe

f = open("John Doe.txt", "w")

string = '''
John Doe is a nice guy. He lives in Nyc and he works with Python
His favorite package is Pandas
'''
f.write(string)

f.close()
```

## 03 Append

```python
# Append to an existing file called John Doe.txt 
# It should add data about John Doe's Hometown

f = open("John Doe.txt", "a")

string = '''
John Doe initially lived in Phoenix, Arizona. He is a very nice guy
'''
f.write(string)

f.close()
```

## 04 Line By Line

```python
f = open("harry.txt", "r")

for line in f:
    print(line)

f.close()
```

## 05 With

```python
# f = open("harry.txt", "r")
# content = f.read()
# print(content)
# f.close()

with open("harry.txt", "r") as f: # context manager
    content = f.read()
    print(content)
    # No need to write f.close() because file is already closed by default when using with synax
```

## 06 Os

```python
import os 


a = os.listdir("dir")
print(a)
print(os.getcwd())
print(os.path.exists("harry"))
# os.remove("sample.txt")
os.rmdir("dir")
```

## 07 Shutil

```python
import shutil

# shutil.rmtree("dir")
# shutil.copy("harry.txt", "john.txt")

shutil.move("john.txt", "dir/")
```

## 08 Argparse

```python
import argparse

parser = argparse.ArgumentParser(description="Simple Calculator")

parser.add_argument("num1", type=float, help="First number")
parser.add_argument("num2", type=float, help="Second number")
parser.add_argument("operation", choices=["add","sub", "div", "mul"], help="Operation to perform")

args = parser.parse_args()

# print(args)

if(args.operation == "add"):
    print(f"The result is {args.num1 + args.num2}")

elif(args.operation == "sub"):
    print(f"The result is {args.num1 - args.num2}")

elif(args.operation == "mul"):
    print(f"The result is {args.num1 * args.num2}")

elif(args.operation == "div"):
    print(f"The result is {args.num1 / args.num2}")

else:
    print("Some error occurred")
 
```

## John Doe

```python

John Doe is a nice guy. He lives in Nyc and he works with Python
His favorite package is Pandas

John Doe initially lived in Phoenix, Arizona. He is a very nice guy

```

## Harry

```python
Hey this is harry and I love python
I am a Pythonista and I love writing code in Python 
I work with AI and Machine Learning Applications
```

# 19 External Modules

## 01 Venv

```python
# v1 - package 1 (pandas)
# v2 - package 2 (numpy)
# v3 - package 3 (moviepy)
#  ".\env2\Scripts\Activate.ps1" (To activate env2)

import moviepy
```

## 02 Requests

```python
import requests

r = requests.get('https://api.github.com/users/codewithharry')

with open("codewithharry.txt", "w") as f:
    f.write(r.text)
```

## 03 Regular Ex

```python
import re
text = "The quick brown fox jumps over the lazy dog."
# https://regexr.com/

# Search for a pattern
# match = re.search("brown", text)
# print(match)
# if match:
#     print("Match found!")
#     print("Start index:", match.start())
#     print("End index:", match.end())

# Find all occurrences of a pattern
# matches = re.findall("the", text, re.IGNORECASE) # Case-insensitive search
# print("Matches:", matches)

new_text = re.sub("fox", "cat", text)
print("New text:", new_text)
```

## 04 Threading

```python
import threading
import time

def worker(num):
    print(f"Thread {num}: Starting")
    time.sleep(2) # Simulate some work
    print(f"Thread {num}: Finishing")

threads = []
for i in range(3):
    thread = threading.Thread(target=worker, args=(i,))
    threads.append(thread)
    thread.start()

for thread in threads:
    thread.join() # Wait for all threads to finish
    
print("All threads completed.")
```

## Codewithharry

```python
{"login":"CodeWithHarry","id":48705673,"node_id":"MDQ6VXNlcjQ4NzA1Njcz","avatar_url":"https://avatars.githubusercontent.com/u/48705673?v=4","gravatar_id":"","url":"https://api.github.com/users/CodeWithHarry","html_url":"https://github.com/CodeWithHarry","followers_url":"https://api.github.com/users/CodeWithHarry/followers","following_url":"https://api.github.com/users/CodeWithHarry/following{/other_user}","gists_url":"https://api.github.com/users/CodeWithHarry/gists{/gist_id}","starred_url":"https://api.github.com/users/CodeWithHarry/starred{/owner}{/repo}","subscriptions_url":"https://api.github.com/users/CodeWithHarry/subscriptions","organizations_url":"https://api.github.com/users/CodeWithHarry/orgs","repos_url":"https://api.github.com/users/CodeWithHarry/repos","events_url":"https://api.github.com/users/CodeWithHarry/events{/privacy}","received_events_url":"https://api.github.com/users/CodeWithHarry/received_events","type":"User","user_view_type":"public","site_admin":false,"name":null,"company":null,"blog":"","location":null,"email":null,"hireable":null,"bio":null,"twitter_username":null,"public_repos":37,"public_gists":3,"followers":29239,"following":0,"created_at":"2019-03-19T04:36:09Z","updated_at":"2025-02-05T08:36:15Z"}
```

## Requirements

```python
c e r t i f i = = 2 0 2 5 . 1 . 3 1 
 
 c h a r s e t - n o r m a l i z e r = = 3 . 4 . 1 
 
 i d n a = = 3 . 1 0 
 
 n u m p y = = 2 . 2 . 3 
 
 p a n d a s = = 2 . 2 . 3 
 
 p y t h o n - d a t e u t i l = = 2 . 9 . 0 . p o s t 0 
 
 p y t z = = 2 0 2 5 . 1 
 
 s c i p y = = 1 . 1 5 . 1 
 
 s i x = = 1 . 1 7 . 0 
 
 t z d a t a = = 2 0 2 5 . 1 
 
 u r l l i b 3 = = 2 . 3 . 0 
 
 
```

# 20 Ai

## 01 String Function

```python
def convert_to_dashed_string(text: str) -> str:
    """
    Converts a given string to a dashed format by:
    - Removing special characters
    - Replacing spaces with dashes
    - Converting the string to lowercase
    """
    # Define allowed characters: alphanumeric and space
    allowed_chars = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789 "
    
    # Remove any character that is not in allowed_chars
    cleaned_text = ''.join(c for c in text if c in allowed_chars)
    
    # Split the cleaned text by spaces and join using dashes
    dashed_text = '-'.join(cleaned_text.split())
    
    # Convert to lowercase for consistency
    return dashed_text.lower()

# Example usage
input_text = "hey  you are good!"
output_text = convert_to_dashed_string(input_text)
print(output_text)  # Output: "hey-you-are-good"

# Additional test cases
print(convert_to_dashed_string("Hello, World!"))  # Output: "hello-world"
print(convert_to_dashed_string("Python@3.9 is great"))  # Output: "python39-is-great"
print(convert_to_dashed_string("   Spaces    everywhere   "))  # Output: "spaces-everywhere"
print(convert_to_dashed_string("123 456 789"))  # Output: "123-456-789"
print(convert_to_dashed_string("MixED cAsE & Special!!"))  # Output: "mixed-case-special"

```

## 02 Tic Tac Toe

```python
# Write code for tic tac toe
# 1. Create a 3x3 board
# 2. Take input from player 1 and player 2
# 3. Check if the input is valid
# 4. Check if the game is over
# 5. Check if the game is a draw
# 6. Check if the game is won
# 7. Print the board after each move
# 8. Print the winner
# 9. Print the draw message
# 10. Print the invalid input message
# 11. Print the game over message

def greet():
    # greet the user 
    print("Good morning! Welcome to Tic Tac Toe!")
    print("Player 1 is X")
    print("Player 2 is O")
    print("Let's start the game!")



def print_board(board):
    for row in board:
        print(" | ".join(row))
        print("-" * 5)

def check_winner(board, player):
    # Check rows, columns and diagonals
    for row in board:
        if all([cell == player for cell in row]):
            return True
    for col in range(3):
        if all([board[row][col] == player for row in range(3)]):
            return True
    if all([board[i][i] == player for i in range(3)]) or all([board[i][2-i] == player for i in range(3)]):
        return True
    return False

def check_draw(board):
    return all([cell != " " for row in board for cell in row])

def main():
    board = [[" " for _ in range(3)] for _ in range(3)]
    current_player = "X"
    game_over = False

    while not game_over:
        print_board(board)
        row = int(input(f"Player {current_player}, enter the row (0, 1, 2): "))
        col = int(input(f"Player {current_player}, enter the column (0, 1, 2): "))

        if row not in range(3) or col not in range(3) or board[row][col] != " ":
            print("Invalid input, please try again.")
            continue

        board[row][col] = current_player


        if check_winner(board, current_player):
            print_board(board)
            print(f"Player {current_player} wins!")
            game_over = True
        elif check_draw(board):
            print_board(board)
            print("The game is a draw!")
            game_over = True
        else:
            current_player = "O" if current_player == "X" else "X"

if __name__ == "__main__":
    main()
```

## 03 LLM API – Reference Notes

This section is just **theory + reference** for how to use an LLM API in Python.
No real API keys should ever be written in code or committed to GitHub.

### 1️⃣ Never hardcode API keys

❌ Do **NOT** do this:

```python
# ❌ Bad practice – never put your real key in code
API_KEY = "your-real-secret-key-goes-here"
```

If this file is pushed to GitHub, your key can be stolen.

---

### 2️⃣ Use environment variables instead

✅ Recommended pattern (concept):

1. Store your key in an environment variable (on your system, not in code).
2. Read that variable in Python using `os.getenv`.
3. Pass it to the client when creating the API object.

Example structure:

```python
import os
from openai import OpenAI  # or any other LLM provider's client

# Reads the key from the environment variable
api_key = os.getenv("OPENAI_API_KEY")

# Create client using the key
client = OpenAI(api_key=api_key)
```

---

### 3️⃣ How to set an environment variable

**Windows (PowerShell):**

```powershell
$env:OPENAI_API_KEY = "your_api_key_here"
python app.py
```

**macOS / Linux (bash / zsh):**

```bash
export OPENAI_API_KEY="your_api_key_here"
python app.py
```

> Replace "your_api_key_here" with your actual key locally,  
> but never commit that value into Git / GitHub.

---

### 4️⃣ Example: basic chat completion flow (pseudo-code)

```python
import os
from openai import OpenAI

api_key = os.getenv("OPENAI_API_KEY")
client = OpenAI(api_key=api_key)

response = client.chat.completions.create(
    model="your-model-name-here",   # e.g., "gpt-4o"
    messages=[
        {"role": "user", "content": "Your prompt goes here"}
    ],
)

reply = response.choices[0].message.content
print(reply)
```

---

### 5️⃣ Best practices summary

- ✅ Use environment variables for keys  
- ✅ Add .env files (if used) to .gitignore  
- ✅ Use placeholders like "your_api_key_here" in docs  
- ❌ Never paste real keys in README, code samples, screenshots, or commits

