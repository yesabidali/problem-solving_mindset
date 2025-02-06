# Task_7: Conditional Statements

Conditional statements make program smart and give ability to make decisions

### if-else 
if-else is a basic of conditional statement.

```py
# Syntax
age = 23
if age>=18:
    print("You can drive")
else:
    print("You can't drive")
```
### if-elif-else
when you have multiple condition we uses elif

```py
# Syntax
age = 23
if age>=18:
    print("You can drive")
elif age==23:
    print("Perfect age to drive")
else:
    print("You can't drive")
```
### Match cases
It is newely introduce in python it is come after python version 10. Working same as if-else but effecity when you have choises it make code readable, easy to maintain and takes less memory compare to if-else

```python

pawd = "abid"

pawd = "abid"

match (pawd):
    case "ali" :
        print("wrong pass")
    case "abcd" :
        print("pass is not that easy")
    case "qwer" :
        print("this is basic pass")
    case "abid" :
        print("correct pass")
    case _:
        print("you dont know the pass")
        
print("ivalid")
```

### Practice:

Write a program which takes student marks as a input and give advide according to there marks

```python

stud_marks = int(input("Write your marks"))
if stud_marks>90:
    print("You are going good")
elif stud_marks>75:
    print("Avrage push your limits")
elif stud_marks>30:
    print("Need lots of work")
else:
    print ("Do hard work")

```

### Memory managements tip for Conditional statements

- Try to avoide making extra branching 
- Try to avoide Memory Allocations in Conditionals
- Use hash table or dict instead of long if-else chains
