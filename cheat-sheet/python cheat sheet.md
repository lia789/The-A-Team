# **Python**

<br>

# Topics need to learn for Python:

```
1. Introduction of python 
2. Operators
3. Input and output statement
4. Flow control
5. String
6. List
7. Tuple
8. Set
9. Dictionary
10.Function
11.Module
12. Package
13.File handling
14.Exception handling/error handling
15.Object oriented program(oop)
16.Polymer phisom
17.Multi trading
18.Building application

```


# **INTRODUCTION OF PYTHON**

<br>

```
Python is a general purpose high level programming language.Python was developed by Guido Van Rossam in 1989 while working at National Research Institute at Netherlands.
```
### Where we can use Python:

```
We can use everywhere. The most common important application areas are
1. For developing Desktop Applications
2. For developing web Applications
3. For developing database Applications
4. For Network Programming
5. For developing games
6. For Data Analysis Applications
7. For Machine Learning
8. For developing Artificial Intelligence Applications
9. For IOT
Note:
Internally Google and Youtube use Python coding
NASA and Nework Stock Exchange Applications developed by Python.
Top Software companies like Google, Microsoft, IBM, Yahoo using Python.

```
# Limitations of Python:
```
1. Performance wise not up to the mark b'z it is interpreted language.
2. Not using for mobile Applications
Python Versions:
Now python have 10+ version running
```
##  Python environment setup:
Install update python
Install text editor vs code
[our professor Lia will install and setup it]

How to write a code:

```python
print("hello world")
#result will shows - hello world


print('this is me Syed Ashraf')
# result will shows - this is me Syed Ashraf


a=10
b=20
z = (a+b)
print(z)
# result will shows- 30

```

# **Identifiers**
```
A name in  Python program is called  identifier.
It can be class name or function name or module name or variable name.
x = 10
```
## Rules to define identifiers in Python:
```
either lower case or upper case
digits(0 to 9)
 underscore symbol(_)
Identifier should not starts with digit
Identifiers are case sensitive.
Can’t use $ or % sign
Can’t use reserve words as a identifiers 
Eg: def=10 
1. If identifier starts with _ symbol then it indicates that it is private
2. If identifier starts with __(two under score symbols) indicating that strongly private
identifier.
3.If the identifier starts and ends with two underscore symbols then the identifier is
language defined special name,which is also known as magic methods.
Eg: __add__
```
# *Reserved Words*
```
 In python there are some words or functionality only used for python for specially built python . These words are called as reserved words. If you use these reserved words as identifier python will mind.
Here we can see all of these:

```
```
Operator type
and ,or , not ,is

Data type
True , False ,None

Control flow 01
If,elif,else

Control flow 02	
while , for , break ,continue, return,in,yield

Exception handling
Try,except,finally,raise,assest

File handling
With,del

[note: Should try to write every reserve words 10 times]

```
# 	Data Types	
<bar>

```Data type means type of data . In python there have some data types , but we can divide them as our own way 2 type 

General data type 
Int ,float,bool,str,none

Excellent data type
 Tuple,set,dict,list

There have some of others(complex,bytes,bytearray,range,frozenset) but according to our job these use case are very short .
```

# Int data type:  it’s a number .Either positive or negative but never be point number


```python
x = 10
type(x)
#result will shows int type
```
# Float data type: it’s a point
 

```python
x = 10.5
type(x)
```
# Bool data type: result will shows True or False
```python
x = 5
y = 6
z = x<6
print(z)
#result wil shows True
```


# Str data type: A String is a sequence of characters enclosed within single quotes or double quotes.
```python s1='ashraf'
s1="ashraf"
a = "bangladesh"
type (a)
#result will shows string type

```

# None data type:result will shows nothing
```python
def m1():
a= 10
print(m1())
#result will shows None
```




# List data type:If we want to represent a group of values as a single entity where insertion order required
``` 
to preserve and duplicates are allowed then we should go for list data type.
1. insertion order is preserved
2. heterogeneous objects are allowed
3. duplicates are allowed
4. Growable in nature
5. values should be enclosed within square brackets
```
```python
l = [1,2,3,4,5,6]
type(l)
#list type
list=[10,20,30,40]
list[0]
#result 10
```


# Tuple data type:tuple data type is exactly same as list data type except that it is immutable.i.e we cannotchage values.Tuple elements can be represented within parenthesis.
```python
t=(10,20,30,40)
type(t)
#tuple type
```

# Set data type:If we want to represent a group of values without duplicates where order is not importantthen we should go for set Data Type. {} second bracket is here identity

```python
s={10,20,30,40}
type(s)
# set type
```

# Dictionary data type: If we want to represent a group of values as key-value pairs then we should go for dict data type.
```
Eg:
d={101:'durga',102:'ravi',103:'shiva'}
Duplicate keys are not allowed but values can be duplicated. If we are trying to insert an
entry with duplicate key then old value will be replaced with new value.
```
```python
d={101:'durga',102:'ravi',103:'shiva'}
type(d)
# dict type
```
# Operators
``` 
Operator is a symbol that performs certain operations
```
## 1. Arithmetic Operators: 
 + ==>Addition
```python
a = 10
b = 6
print(a+b)
#result 16
```
- ==>Subtraction
```python
a = 10
b = 6
print(a-b)
#result 4
```
* ==>Multiplication
```python
a = 10
b = 6
print(a*b)
#result 60
```
 ==>Division operator
```python
a = 10
b = 5
print(a/b)
#result 2
```
% ===>Modulo operator
```python
a=10
b=2
print('a%b')
#result a%b
```
// ==>Floor Division operator
```python
a = 10.5
b=2
print(a//b)
#result will 5
```
# 2.Relational Operators:
```
>
```
```python

x = 9
y = 6
z = x>6
print(z)
#true
```
```
>=
```
```python
x = 9
y = 6
z = x>=6
print(z)
```
```

<
```
```python
x = 3
y = 6
z = x<6
print(z)
```
```
<=
```
```python
x = 3
y = 6
z = x<= 6
print(z)
```
# 3.Logical Operators:

## and

```python
"habib" and "ashraft"
# “habibashraf”
```
## or 

```python

a = "" or "lia"
print(a)
#lia
```


## not
```python
is_raining = False
if not is_raining:
   print("It is not raining. You can go outside without an umbrella.")
else:
   print("It is raining. Don't forget your umbrella!")
#It is not raining. You can go outside without an umbrella.
```
# 4.Bitwise Operators:
```
We can apply these operators bitwise.
These operators are applicable only for int and boolean types.
By mistake if we are trying to apply for any other type then we will get Error.
```
```
&
```
```python
a = 12 
b = 10 
result = a & b
print("The result of a & b is:", result)
#The result of a & b is: 8
```
```
|
```
```python
a = 12
b = 10 
result = a | b
print("The result of a | b is:", result)
#The result of a | b is: 14
```
```
^
```
```python
a = 12  # In binary: 1100
b = 10  # In binary: 1010


# Perform bitwise XOR operation
result = a ^ b


# Print the result
print("The result of a ^ b is:", result)
#The result of a ^ b is: 6
```
```
<<
```
```python
a = 3 
result = a << 2
print("The result of a << 2 is:", result)
#The result of a << 2 is: 12
```
```
>>
```
```python
a = 3 
result = a >> 2
print("The result of a << 2 is:", result)
#The result of a << 2 is: 0
```

# Input And Output Statements
```
Input and output statements are fundamental in programming as they allow a program to interact with the user or other systems by receiving data (input) and providing data (output)
```
## Input Statements
Input statements are used to get data from the user or another source.
```python
# Prompt the user to enter their name
name = input("Enter your name: ")
print("Hello, " + name + "!")
#Hello, !
```
```
In this example, input("Enter your name: ") prompts the user to enter their name and stores the input as a string in the variable name.
```


## Output Statements in Python
```
To display output to the user, Python provides the print() function. This function prints the specified message to the screen or other standard output devices.
```
```
Simple Output:
```
```python
print("Hello, world!")
#Hello, world!
```

## Output with Variables:
```python
age = 25
print("I am", age, "years old.")
#I am 25 years old.
```
## Formatted String Output:
```python
name = "Alice"
age = 25
print(f"My name is {name} and I am {age} years old.")
#My name is Alice and I am 25 years old.
```
# Command Line Arguments
```
In Python, command line arguments are parameters passed to your script when it's executed from the command line or terminal. They can be used to influence the behavior of the script without altering the code. Python provides several ways to handle these arguments.
Basic Example Using sys.argv
The sys.argv list in the sys module is the simplest way to handle command line arguments. The first element (sys.argv[0]) is the name of the script, and the subsequent elements are the arguments passed.
```



```python
import sys


if len(sys.argv) < 2:
   print("Please provide an argument")
else:
   print("Argument 1:", sys.argv[1])
```

# Flow Control
```
Flow control in programming refers to the mechanisms that dictate the order in which statements, instructions, or function calls are executed or evaluated .flow control structures enable you to manage the direction your code takes, including making decisions, repeating actions, or executing code based on certain conditions.
```
```
Key Flow Control Structures in Python
Conditional Statements: if, elif, else
These statements allow you to execute certain blocks of code based on whether a condition is True or False.
```
```python
age = 25
if age >= 18:
   print("You are an adult.")
elif age >= 13:
   print("You are a teenager.")
else:
   print("You are a child.")
#You are an adult.
```

# Loops: for and while
```
Loops are used to repeat a block of code multiple times.
```
# for Loop:
```
 Iterates over a sequence (like a list, tuple, string, or range) and executes a block of code for each element in the sequence.
```
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
   print(fruit)
#apple
Banana
cherry
```
# while Loop: Repeats a block of code as long as the condition is true.
```python
count = 0
while count < 9:
   print(count)
   count += 1
#0
1
2
3
4
5
6
7
8
```


##  Control Flow Tools: break, continue, pass
```

These tools provide additional control within loops and conditional statements.
break: Exits the nearest enclosing loop prematurely.
```
```python
for i in range(10):
   if i == 5:
       break
   print(i)
#0
1
2
3
4
```

## continue: 
```
Skips the rest of the code inside the loop for the current iteration and moves to the next iteration.
```
```python
for i in range(10):
   if i % 2 == 0:
       continue
   print(i)
#1
3
5
7
9
```

## pass: 
```
Does nothing and is often used as a placeholder for future code.
```
```python
for i in range(5):
   pass  # Placeholder for code that hasn't been written yet
```



# String Data Type
```
Strings in python are surrounded by either single quotation marks, or double quotation marks.
'hello' is the same as "hello".
You can display a string literal with the print()
```
```python
print("He is called 'Johnny'")
print('He is called "Johnny"')
He is called 'Johnny'
He is called "Johnny"
```

## Assign String to a Variable:
```python
a = "Hello"
print(a)
```

## Multiline Strings
```python
a = """Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua."""
print(a)

#Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua.
```

# Strings are Arrays
```python
a = "Hello, World!"
print(a[1])
#e
```

## Looping Through a String
```python

for x in "banana":
 print(x)
#b
a
n
a
n
a
```
## String Length
```python
a = "Hello, World!"
print(len(a))
#13
```


# Slicing Strings:

```
You can return a range of characters by using the slice syntax.
Specify the start index and the end index, separated by a colon, to return a part of the string.
{Get the characters from position 2 to position 5 (not included)}
```
```python
b = "Hello, World!"
print(b[2:5])
#llo
```
```
Get the characters from position 2, and all the way to the end:
```
```python
b = "Hello, World!"
print(b[2:])
#llo, World!
```

## Negative Indexing
```python
b = "Hello, World!"
print(b[-5:-2])
#orl
```
## Upper Case
```python
a = "Hello, World!"
print(a.upper())
#HELLO, WORLD!
```
## Lower Case
```python
a = "Hello, World!"
print(a.lower())
#hello world
```

## Remove Whitespace
```python
a = " Hello, World! "
print(a.strip()) # returns "Hello, World!"
#Hello, World!
```
## Replace String
```python
a = "Hello, World!"
print(a.replace("H", "J"))
#Jello, World!
```
## Split String
```python
a = "Hello, World!"
print(a.split(",")) # returns ['Hello', ' World!']
#['Hello', ' World!']
```
## String Concatenation
```python
a = "Hello"
b = "World"
c = a + b
print(c)
#HelloWorld
```
```python
a = "Hello"
b = "World"
c = a + " " + b
print(c)
#Hello World
```

## F string
```python
age = 36
txt = f"My name is John, I am {age}"
print(txt)
#My name is John, I am 36
```

# List Data Structure
```
Lists are used to store multiple items in a single variable. Lists are created using square bracket:
   ```
## Create a List:
```python
thislist = ["apple", "banana", "cherry"]
print(thislist)
#['apple', 'banana', 'cherry']
```


## Lists allow duplicate values:
```python
thislist = ["apple", "banana", "cherry"]
print(thislist)
#['apple', 'banana', 'cherry']
```
thislist = ["apple", "banana", "cherry"]
print(len(thislist))
#3



String, int and boolean data types:
list1 = ["apple", "banana", "cherry"]
list2 = [1, 5, 7, 9, 3]
list3 = [True, False, False]
Remove Specified Item:
thislist = ["apple", "banana", "cherry"]
thislist.remove("banana")
print(thislist)
#['apple', 'cherry']

If there are more than one item with the specified value, the remove() method removes the first occurrence:
thislist = ["apple", "banana", "cherry", "banana", "kiwi"]
thislist.remove("banana")
print(thislist)
#['apple', 'cherry', 'banana', 'kiwi']

Remove the second item:
thislist = ["apple", "banana", "cherry"]
thislist.pop(1)
print(thislist)
#['apple', 'cherry']


Remove the last item:
thislist = ["apple", "banana", "cherry"]
thislist.pop()
print(thislist)
#['apple', 'banana']
Remove the first item:
thislist = ["apple", "banana", "cherry"]
thislist.pop(1)
print(thislist)
#['banana', 'cherry']
Delete the entire list:
thislist = ["apple", "banana", "cherry"]
del thislist
#
Clear the list content:
thislist = ["apple", "banana", "cherry"]
thislist.clear()
print(thislist)
#[]
Print all items in the list, one by one:
thislist = ["apple", "banana", "cherry"]
for x in thislist:
 print(x)
#apple
banana
cherry


