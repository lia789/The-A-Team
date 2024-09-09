## **03. Python Syntax Questions**

### **Question 1**
```python
"""
Fix indentation, colons, and function definition: The following code is supposed to define a function that checks whether a number is even or odd, but it has multiple syntax errors related to indentation, colons, and return statements. Can you fix it?
"""

def check_even_odd(number)
    if number % 2 == 0
    print(f"{number} is even.")
    else
    print(f"{number} is odd.")
    return number
result = check_even_odd(10)
```

### **Question 2**
```python
"""
Correct string formatting and syntax issues: The code below is intended to display a message depending on the score. Fix the issues related to incorrect string formatting, comparison operators, and print statements.
"""
def display_message(score):
    if score > 90:
    print("Congratulations! You got an A!")
    elif score >= 80
    print(f"Good job! Your score is {score}.")
    else
    print("Keep trying!")

display_message(85)
```


### **Question 3**
```python
"""
Fix the issues with for loop and syntax errors: The following code intends to print the sum of numbers in a list. It has syntax errors in the loop and function definition. Can you fix them?
"""
def calculate_sum(numbers)
    total = 0
    for num in numbers
        total += num
    return total

num_list = [10, 20, 30, 40]
result = calculate_sum(num_list)
print(f"The sum is {result}")
```


## **04. Variables and Constants Questions**

### **Question 1**
```python
"""
Fix variable assignment and constant definition: The code below is calculating the area of a rectangle but misuses variables and constants. Fix the issues by correctly assigning variables and ensuring that the constant value remains unchanged throughout the code.
"""
length = 10
WIDTH = 20
length = 15 # Changed length for a new rectangle
area = LENGTH * WIDTH
print(f"Area of rectangle: {area}")

WIDTH = 30  # This should not change since WIDTH is a constant
area = length * WIDTH
print(f"New area of rectangle: {area}")
```

### **Question 2**
```python
"""
Avoid reusing variable names incorrectly: This program calculates the volume of a cylinder. There's an issue where variable names are reused inappropriately, and constants aren't defined properly. Fix the code to maintain good naming practices.
"""
radius = 5
height = 10
pi = 3.1415  # Pi should be treated as a constant
area = 2 * pi * radius * height + 2 * pi * radius * radius
print(f"Surface area of cylinder: {area}")

volume = pi * radius * radius * height
print(f"Volume of cylinder: {volume}")

pi = 3.14  # This should not happen since pi is a constant
```

### **Question 3**
```python
"""
Fix multiple variable assignments and prevent overwriting: The following program calculates the total price of items in a shopping cart. There's an issue with overwriting variables and improper assignment of constants. Correct the issues to ensure that the calculations work properly.
"""
item_price = 20
quantity = 5
discount = 0.1
total_price = item_price * quantity
print(f"Total price without discount: {total_price}")

total_price = total_price - (total_price * discount)  # Applying discount
print(f"Total price with discount: {total_price}")

DISCOUNT = 0.2  # This discount should remain constant throughout
total_price = item_price * quantity - (total_price * DISCOUNT)
print(f"Total price with updated discount: {total_price}")
```


## **05. Identifiers Questions**
### **Question 1**
```python
"""
Fix invalid variable names: The following code contains incorrect variable names that don’t adhere to Python’s naming conventions. Correct the invalid variable names.
"""
1st_value = 100
@name = "John"
total$amount = 2000
print(1st_value, @name, total$amount)
```

### **Question 2**
```python
"""
Avoid reserved word usage: The code below uses a reserved word as a variable name, which is not allowed in Python. Can you fix the variable name to follow Python's identifier rules?
"""
def = 50
sum = def + 100
print(f"The sum is: {sum}")
```
### **Question 3**
```python
"""
Correct naming style: The code below does not follow Python’s recommended naming conventions (PEP 8). Modify the variable names to follow proper conventions.
"""
TOTALSUM = 1000
PriceOfItem = 200
discountValue = 50
print(TOTALSUM, PriceOfItem, discountValue)
```

## **06. Reserved Words Questions**
### **Question 1**
```python
"""
Identify the issue with reserved words: The code below uses reserved keywords improperly in variable names. Fix the issues and explain why they can't be used.
"""
for = 10
if = 20
return = 30
print(for, if, return)
```

### **Question 2**
```python
"""
Correct improper reserved word usage: The following code attempts to use reserved words in function names. Fix the issue by renaming the functions.
"""
def class():
    return "This is a class function"

def import():
    return "This is an import function"

print(class())
print(import())
```

### **Question 3**
```python
"""
Avoid using reserved words for variable assignment: The following program incorrectly assigns values to reserved words. Fix the variable names to adhere to Python's naming rules.
"""
try = 100
except = 50
finally = try + except
print(finally)
```


## **07. Data Types Questions**

### **Question 1**
```python
"""
Correct data types usage: The code below contains incorrect data types for some variables. Fix the errors and ensure the correct data types are used.
"""
name = 12345  # Name should be a string
age = "25"  # Age should be an integer
price = '100.50'  # Price should be a float
print(name, age, price)
```

### **Question 2**
```python
"""
Ensure consistent data types in calculations: The code below uses mixed data types that cause errors during calculation. Correct the code to avoid type mismatch errors.
"""
length = "5"
width = 10
area = length * width
print(f"Area: {area}")
```

### **Question 3**
```python
"""
Fix issues with data type conversion: The following code performs operations on variables without converting their data types properly. Fix the data type conversion errors.
"""
x = "10"
y = 20
sum = x + y  # This will cause a type error
print(f"The sum is: {sum}")
```

## **08. Type Conversion Questions**
### **Question 1**
```python
"""
Correct type conversion: The following code attempts to concatenate a string and integer without converting the data type. Fix the type conversion error.
"""
age = 25
message = "You are " + age + " years old."
print(message)
```

### **Question 2**
```python
"""
Ensure correct type casting: The code below uses incorrect type casting. Correct the casting issues to avoid runtime errors.
"""
x = "50"
y = 25
result = int(x) + str(y)  # Incorrect casting here
print(result)
```

### **Question 3**
```python
"""
Handle float and string conversion: The following code contains type conversion errors when dealing with float and string types. Fix the type conversion issues.
"""
price = 100.75
message = "The price is " + price
print(message)
```

## **09. Operators Questions**
### **Question 1**
```python
"""
Fix operator precedence issues: The following code does not follow proper operator precedence. Modify the code to ensure correct calculation.
"""
result = 10 + 5 * 2 - 3 / 2
print(f"Result is: {result}")
```

### **Question 2**
```python
"""
Correct comparison operator usage: The code below uses incorrect comparison operators, resulting in logical errors. Fix the comparison operators to make the logic correct.
"""
age = 20
if age => 18:
    print("You are an adult.")
else:
    print("You are a minor.")
```

### **Question 3**
```python
"""
Correct logical operator usage: The following code incorrectly uses logical operators. Fix the issues to ensure the correct conditions are evaluated.
"""
x = 10
y = 20
if x > 5 or y < 10 and x == 10:
    print("Condition met!")
else:
    print("Condition not met.")
```

## **10. Input and Output Questions**
### **Question 1**
```python
"""
Fix input function usage: The following code does not correctly handle user input and performs improper type conversion. Fix the code to correctly accept user input and process it.
"""
age = input("Enter your age: ")
if age >= 18:
    print("You are eligible to vote.")
else:
    print("You are not eligible to vote.")
```

### **Question 2**
```python
"""
Ensure formatted output: The following program doesn’t use formatted output correctly. Modify the print statements to ensure proper formatting.
"""
name = "Alice"
score = 95
print("Name: " + name + ", Score: " + score)
```


### **Question 3**
```python
"""
Fix input validation: The following program doesn't correctly validate user input. Modify the program to ensure the input is properly handled and validated.
"""
age = int(input("Enter your age: "))
if age.isdigit():
    print(f"You are {age} years old.")
else:
    print("Invalid age entered.")
```


