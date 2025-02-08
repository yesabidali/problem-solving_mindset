# Error Handling in Python – try, except, finally
When writing a program, sometimes errors occur. Error handling helps the program from crashing by managing errors properly

Python provides the try, except, and finally blocks to handle errors.

### What is try, except, and finally?
Keyword	use
- try: Runs the code that may cause an error
- except: Handles the error if it occurs
- finally: Always runs, whether an error occurs or not

### How Does Error Handling Work?

Example Using try and except

```python
try:
    number = int(input("no likho: "))  # User enters a value
    print("You entered:", number)
except ValueError:  # Handles wrong input
    print("no galat hai")
```

### Using Multiple except Blocks
We can handle different errors separately
```python
try:
    x = int(input("no likho: "))
    result = 10 / x  # This cause ZeroDivisionError
    print("Result:", result)
except ValueError:
    print("galt no sahi no likho")
except ZeroDivisionError:
    print("matlab kuch bhi zero se divide kar rahe ho")

```
### Using finally Block
Finally block always runs, even if an error occurs

```python
try:
    num = int(input("no liko: "))  # User enters a number
    print("tumne no dala hai:", num)
except ValueError:
    print("yeh no nhi hai")  # Handles invalid input
else:
    print("kuch bhi error nhi")  # Runs if no error
finally:
    print("dhanyawaad")  # Runs always
