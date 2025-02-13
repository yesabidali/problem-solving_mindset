# What is class?
Class provide blue print or template to object it is like sturucture

# Why we are using class?
We uses class to organized, reuse, and maintain the code and for hiding our code

# Does Class really reduce the line of code?
No class donot reduce the line of code but using classes can reduce code duplication, making it easier to extend and maintain. In some task function is more straight forward

# What is object?
Object is instance of class we are doing actual implementation in object

# Attribute 
Attribute are variable that store in class

# Constructor
Constructor is special method that automatically called when an object is created 
Main purpose is to allocate memory and intilize an object 
some constructor are: (_ _new_ _ ), (_ _ str __)

# Does init is really constructor and what is meaning __ (double under score in constructor)
No init is not actually constructor it is intilizer used to intilize where as (__) double underscore. It is a dunder method it define the behaviour of your object 

# Syntax
```python
class Bus_details: # class is reserved keywor used for making class and Bus_details is class name here
    def __init__(self,bus_no, destination, status="on the way"): # init is initilizal and some attribute
        self.bus_no = bus_no # Assigning value
        self.destination = destination # Assigning value
        self.status = status  # Assigning value
    def display(self): # Creating Display method
        print(f"Bus no is {self.bus_no} | Destination is {self.destination} | Status is {self.status}")
    def update(self, new_status): # Creating update method
        self.status = new_status # updating status
        print(f"The new status is {self.status}")
busobject = Bus_details("Forteen","Gandhi Path Mode") # creating objects
busobject.display() # Calling method
busobject.update("Your missed out") 
busobject2 = Bus_details("Nine B","Raja Park")
busobject2.display()
```
# Questions:

### Q.1 Can we define a class without using class keyword in python ?

Yes we can define class without using class keyword if can use type() keyword The type() function can be used to create a class at runtime but using class more beneficial as class it increase readablity of code and we can use class features in it

### Q.2 What is difference between class variable and instance variable?

A Variable that can share among all class is called class variable and class variable can only shared among class 

```python

class Car:
    # Class variable (shared by all instances)
    body = "metal"

    def _init_(self, brand, color):
        self.brand = brand
        self.color = color

# Creating object
car1 = Car("Toyota", "Red")
car2 = Car("Honda", "Blue")

# Accessing instance variables
print(car1.brand, car1.color)  # Toyota Red
print(car2.brand, car2.color)  # Honda Blue

# Accessing class variable
print(car1.body)  # metal
print(car2.body)  # metal

# Modifying class variable
Car.wheels = "Carbon Fibre"  # Changes for all instances
print(car1.body)  # carbon fibre
print(car2.body)  # carbon fibre

# Modifying instance variable
car1.color = "Black"
print(car1.color)  # Black
print(car2.color)  # Blue (remains unchanged)
```
### Q.3 We know _init_ constructor used for initialize the object attributes and what happens when we don't use this init constructor?


### Q.4 If inside init method we don't write self then what will be happen?

Without self you can't refer the object and error will occur telling position agrument

```python
class Example:
    def __init__(name, age):  # Missing 'self'
        name.age = age  # This will cause an error

obj = Example("John", 25)
```

### Q.5 Why we are making methods in every class if I want to use addition so I made a addition function and why don't I use that function in the class ? it takes less memory space and also fasten the program?

It depend on situation what is our purpose like if your concern is memory then you can make additional function if you want to hide your method then you can make in class. But you should avoide it because it is not good practice it decrease the readability and make code complex increase debugging issue and generate logs
```python

class MyClass:
    pass

def my_function():
    return "Hello"

MyClass.func = my_function
print(MyClass.func())  # Output: Hello
```
### Q.6 Does _ _init_ _ are actually constructor and what is meaning of double underscore in this?

No, _ _init_ _ is not a constructor in Python. It is an initializer.

A constructor is a special method responsible for creating an object in memory. In Python, the real constructor is _ _new_ _ , while _ _init_ _ only initializes the already-created object.

Where as (__) double underscore is a special method. It is a dunder method it define the behaviour of your object dunder method actomatically call when object is created

### Q.7 What will happen when we assign one object to another object?

```python
class Abid:
    def __init__(self, name):
        self.name = name

p1 = Abid("Alice")
p2 = p1  # Assigning p1 to p2

p2.name = "Bob"  # Modifying p2 also changes p1

print(p1.name)  # Output: Bob
print(p2.name)  # Output: Bob
```
It come here concept of shallow and deep copy if two object is assign to each other both object have same refrance in memory

### Q.8 For calling an object we need (.) operator why we are using (.), can we call the object like variables_module(display_info())

### Q.9 What happen if we don't write object in class or can we write multiple objects in one class. Does object is only using for creating instance of class or we can do more things with objects? 

If you don't create an object of a class, the class will just exist as a blueprint, but you won't be able to interact with its data or methods (attributes and behaviors). 

```python
class Abid:
    def __init__(self, name, age):
        self.name = name
        self.age = age

# Defining a class without creating an object
# No object has been instantiated here, so we cannot access 'name' or 'age'
```

Yes we can multiple obejects in class
```python
class Bus_details: 
    def __init__(self,bus_no, destination, status="on the way"): 
        self.bus_no = bus_no 
        self.destination = destination 
        self.status = status  # Assigning value
    def display(self): 
        print(f"Bus no is {self.bus_no} | Destination is {self.destination} | Status is {self.status}")
    def update(self, new_status): # Creating update method
        self.status = new_status # updating status
        print(f"The new status is {self.status}")
busobject = Bus_details("Forteen","Gandhi Path Mode") # creating objects
busobject.display() # Calling method
busobject.update("Your missed out")  
busobject2 = Bus_details("Nine B","Raja Park") # Multiple object
busobject2.display()
```
