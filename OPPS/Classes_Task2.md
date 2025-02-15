# Constructors, Instance Variables & Methods

## What is Instance Variable?
Instance variable ek aesa variable hota hai jo class ke andar define hota hai, lekin har object ke liye alag-alag hota hai Ye variables self keyword ke sath define kiya jata hain aur object (instance) ke data ko store karne ke liye use hoti hain Instance Variable access hota hai dot operator ki madat se

```python
class Bottle():
    def __init__(self,body,type):
        self.body = body # variable instance
        self.type = type # variable instance
bottleobject = Bottle("metal", "waterbottle")
bottleobject1 = Bottle("plastic", "Tea bottle")       
print(f"The body is {bottleobject.body} and type of bottle is {bottleobject.type}")
print(f"The body is {bottleobject1.body} and type of bottle is {bottleobject1.type}")
```

## What is Dot operator doing in python class?

Yeh instance variable ko access karne ke kaam aata hai aur method ko call karne ke 

## Can I make instance variable with making a constructor?

Yes we can make instance variable without making constructor

```python

class Kuchbhi():
    pass
object = Kuchbhi()
object.kya = "Pana nhi"
object.study = "Full focus"
print(object.kya , object.study)
```
## Operator overloading aur Method overloading

Same operator diffrent behavior hota aise hi method overloading hota same method but diffrent behaviour
## What is Constructor?

Python mai constructor ek special method hota hai jo kisi class ke object banate time automatically call ho jata hai constructor ka mai purpose object ko intiliaze karana hota hai aur value allocate karna hota hai

Types of Construtor 
- Default Constructor
- Parametarize Constrctor
- Constructor with default Values

Default Constructor : Jab aap constructor ko bina kisi artibute ke banate ho toh vo default contructor hota hai


```python
class Human():
    def __init__(self):
        self.boy = "Rakesh"
        self.girl = "Rina"

object = Human()
print(object.boy)
print(object.girl)
```

Parametarize Constructor: In this constructor we give artibute to constructor

```python
class Bottle():
    def __init__(self,body,type):
        self.body = body # variable instance
        self.type = type # variable instance
bottleobject = Bottle("metal", "waterbottle")
bottleobject1 = Bottle("plastic", "Tea bottle")       
print(f"The body is {bottleobject.body} and type of bottle is {bottleobject.type}")
print(f"The body is {bottleobject1.body} and type of bottle is {bottleobject1.type}")
```
Constructor with default Values: Isme hum parameter ke sath default values di jata hai

```python
class Person:
    def __init__(self, name="Unknown", age=0):
        self.name = name
        self.age = age

person1 = Person()         # Default constructor call
person2 = Person("Abid", 21)  # Parameterized constructor call

print(person1.name)  # Output: Unknown
print(person1.age)   # Output: 0
print(person2.name)  # Output: Bob
print(person2.age)   # Output: 35
```
## What is decorator?

@ symbol ka use Python mein decorators ko define karne ke liye hota hai Decorators ek special type ka function hote hain jo dusre functions ya methods ko modify karte hain, ya unka behavior change karte hain. @ symbol decorator ko apply karne ka syntax hai

Decorator code ko reusable banane hai help karta hai
## What is alternative constructor

Alternative constructor ek class method hota hai jo @classmethod decorator ka use karke banaya jata hai Ye class ke multiple ways se object create karne ki flexibility provide karta hai

## What is methods?

Method ek function hota hai jo kisi specific object ya class ke saath associated hota hai methods ko class ke andar define kiya jaata hai aur wo class ke objects ke behaviors ko define karte hain In short methods wo actions hote hain jo class ke objects perform kar sakte hain

Types of method
- Instance method
- Class method
- Static method

Instance method : Yeh method object ke through call hote hai aur yeh self keyword ka use karte hai
```python
class Person:
    def __init__(self, name="Unknown", age=0):
        self.name = name
        self.age = age

person1 = Person()         # Default constructor call
person2 = Person("Abid", 21)  # Parameterized constructor call

print(person1.name)  # Output: Unknown
print(person1.age)   # Output: 0
print(person2.name)  # Output: Bob
print(person2.age)   # Output: 35
```

Class method : Class method vo method hote hai jo class ke saath related hote hain na ki specific object ke saath Class methods ko call karte waqt class ko pass kiya jaata hai aur isliye in methods ka pehla parameter cls hota hai jo class ka reference hota hai yeh cls keyword ka use karte hai

yeh class level ka data access ya modify karne ke kaam aata hai

```python
class Bag():
    kitnebag = 0

    def __init__(self, brand , color):
        self.brand = brand
        self.color = color
        Bag.kitnebag +=1

    @classmethod
    def bataokitne(cls):
        print(f"bag itne hai {cls.kitnebag}")
object1 = Bag("Oslika", "Brown")
object2 = Bag("HP", "Grey")
print(f"bag ka brand hai {object1.brand} aur color yeh hai {object1.color}" )
Bag.bataokitne()
```

Static method: Static methods wo methods hote hain jo na to class ke instance, na hi class ke state ko access karte hain. In methods ka pehla parameter na self hota hai, na cls. Ye methods independent hote hain aur inhe class ya instance se directly call kiya jaata hai

```python
class Staticmethodkause():

    @staticmethod
    def add(a,b):
        num = a+b
        return (num)
    @staticmethod
    def minus(x,y):
        num2 = x-y
addkaro = Staticmethodkause.add(99,23)
minuskaro = Staticmethodkause.minus(90, 23)
print(addkaro)
print(minuskaro)
```

## Practice of class

Make a class student which marks and name as attribute and give you grade based on marks

```python
class Student():
    def __init__(self, name, marks):
        self.name = name 
        self.marks = marks
    def grade_assign(self):
        if self.marks >= 90:
            print (f"your marks is {self.marks}you got A grade")
        elif self.marks >= 80 :
            print (f"your marks is {self.marks}you got B grade")
        elif self.marks >= 50 :
            print (f"your marks is {self.marks}you got C grade")
        else :
            print ("Fail")

object1 = Student("Abid", 90)
object2 = Student("sorav", 90)
object3 = Student("raghav", 90)
object1.grade_assign()
object2.grade_assign()
object3.grade_assign()
```

```python

    def __init__ (self ,product_name, price, quantity ):
      self.product_name = product_name
      self.price = price
      self.quntity = quantity
    def calculate(self,):
       total = self.quntity * self.price
       print((f"your total price is {total}"))
       
object1 = Shopping_cart("Apple", 60, 60 ) 
object2 = Shopping_cart("bana", 23, 100 ) 
object1.calculate()
object2.calculate()
```
