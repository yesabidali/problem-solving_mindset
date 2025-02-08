# Lambda Function

Function that can have any number of arguments but only one expression 

## Syntax of Lambda function

```python
 lambda arguments: expression
```
- Lambda is keyword reserved for lambda function
- It can take multiple arguments
- No need to write return 

```python
# Regular function

def abid_add(a):
    return a * a
abid_add(2)

```

```python

# Lambda function 
mul_lambda = lambda a: a * a

mul_lambda(5) # Output: 25

```
Lambda dunction helps to reduce line of code and it is great for one-time-use functions
