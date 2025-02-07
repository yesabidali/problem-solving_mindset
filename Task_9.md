# While loops 
While loops checks condition first then execute or doing retative task until condition is true 

```python
abid_fav_sweet = " "
while abid_fav_sweet != "kaju katli":
    abid_fav_sweet = input("This is not abid fav sweet")
print("Yes you are right this is abid fav sweet")

```

```python
# what is problem in this code?
num = 1
while num>1:
    num = num+1
    print(num)

```
```python
num = 1
while num<10:
    num = num+1
    print(num)
```

# Using While True, Continue and break
- While True it is a infinite loops
- Break is use to break the itration
- Continue is used to skip the current iteration and move to the next loop cycle

```python
while True:
    passd = input("Write your passwd: ")
    if passd == "meranaamabidhai":
        break
print("you entre right passwd")
```

```python
for num in range(1, 6):  
    if num == 3:
        continue  # Skip number 3
    print(num)
```

```python

# Using enumerate() Instead of range(len())
# shoe = ['bata', 'puma', 'nike', 'addidas']
# for abid in range(len(shoe)):
#     print (abid, shoe[abid])

shoe = ['bata', 'puma', 'nike', 'addidas']
for abid, ali in enumerate(shoe):
    print (abid, ali)

```
