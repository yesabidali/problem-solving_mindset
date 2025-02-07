# Funtions with parameters

By giving parameters you can make code resuable and avoide hardcoding

Examples:

```python
def add(a,b):
    sum = a+b
    print(f"the sum of a+b is {a}{b}")
add(4 ,5) 
```

```python

def calculate_discount(price, discount):
    discnt = (price*discount)/100
    print(f"you discount price is: {discnt}")
calculate_discount(500,17)

```
```python

Function with Return Values
def add(a, b):
    return a + b

goal = add(56, 10)
print("Sum:", goal)

```
# Local Variable:
A local variable is a variable declared inside a function and is only accessible within that function. It cannot be used outside the function

# Global Variable:
A global variable is a variable declared outside any function, making it easu to access the entire program, including inside functions

```python
def greet():
    greet_abid = "Hello, I am a local variable!"  # Local variable
    print(greet_abid)

greet()  
print(message)  #  This will cause an error because greet_abid is local

```
```python
greet_abid = "Hello, I am a global variable!"  # Global variable

def greet():
    print(greet_abid)  

greet()
print(greet_abid) 

```
