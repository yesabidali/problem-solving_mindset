# Loops

It allowing you to execute repetitive tasks efficiently. To repeat a task multiple times without writing the same code again and again. Loops make our code shorter, faster, and easier to manage

# Why I am only using loops to perform repetative task if there are other methods also?

Loop are not only way do to repatative tasks we have Recursion, Vectorized operations, Map, filter, and list comprehension 
all have there unique use but we are using loops because it works on almost every situation either we have small data or complex data , Loops make code readable consume less memory easy to debug and maintain code 

# What is meaning of Iterate or Iteration?

Iterate" means to go through something step by step, one at a time
Like fliping page of note one after or moving up to stair step by step or going to 1 to 10 numbers one after another

### Syntax For loops

```python

companies = ["google","microsoft", "IBM", "amazon", "nvidia"]
for company in companies:
     print(company)
```
What if I have to print only first 3 company names or last 2 names for doing this we have to use range function
```python
companies = ["google","microsoft", "IBM", "amazon", "nvidia"]
for i in range(3):
     print(companies[i])

companies = ["google","microsoft", "IBM", "amazon", "nvidia"]
for company in companies[-4:]:
     print(company)
```
  range(start, stop, step)

  ```python
  for _ in range(1,40,3):
    print(_)
```
```python
# Program to print table

num = int(input("Write the number "))
for i in range(1,11):
    print(i*num)
 ```
### Practice

```python
learning_topics = ['basic_programing', 'java_script', 'AI', 'ML']
for learn in learning_topics:
    print(learn)
```
