# Modules and Importing

Modules is a file which some contain pre writen code. Modules help in organizing code, improving reusability, and making programs easier to maintain. There built in module and also we can create our own module

## Why we are Using Modules?

We use modules 
- To reuse the code, 
- To avoide the hardcoding, 
- For using built in function and 
- For hiding our code

## How to module in Python
We need to import the module by writing the keyword "import"

## Importing built in module

```python
import math
print(math.sqrt(100000))
```

```python
import math

print(math.sqrt(78)) #Square root
print(math.pow(2, 3)) #power
print(math.factorial(68)) # Factorial
print(math.pi)   # Pi value
print(math.log(10))  # Log
```

```python
# Date abd Time

import datetime

current_datetime = datetime.datetime.now() # Current time
print("current date and time:", current_datetime)

today_date = datetime.date.today() # today date
print("Today's Date:", today_date)

custom_date = datetime.datetime(2025, 2, 8, 10, 30, 45) # custom date
print("Custom Date & Time:", custom_date)
```
```python
### Making own module

Creating own module abid_module.py:

def greet(name):
    return f"Hello, {name}!"

using it in another file

import my_module
print(my_module.greet("Abid")) 
```

