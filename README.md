 # brocode's python full course notes 🐍♥️
> these are my notes from BroCode's python course on youtube, formatted in markdown for readability. i'm creating these notes to refer back to them in the future, and they might also benefit others following the course. good luck to everyone!
 
 ## 🔗 [course link](https://youtu.be/XKHEtdqhLK8?si=IqUga8mt5dGJ7x4i) 
## 01. print function 
```python
print("hello world")
```
## 02. variables
- a **variable** is a container for a value, it behaves as the value that it contains.
### ♥️ strings
```python
name = "Bro"
print(type(name))
print("Hello " + name)
```

```python
first_name="Bro"
last_name="Code"
full_name=first_name + last_name
print("Hello "+ full_name)
``````
### ♥️ integers
```python
age = 21
# to increment
age +=1 
print(age)
print('Your age is: '+str(age))
```
> when assigning value for integer type variables we do **not** use quotes as strings are not used in math.
### ♥️ float
```python
height=250.5
print(height)
```
### ♥️ boolean
> can only store **True** or **False** values
```python
human = False
print(human)
```
- use the '**type**' function to find variable data type

```python
print(type(name))
print(type(age))
print(type(height))
print(type(human))
```
## 03.multiple assignment
- **multiple assignment** allows us to assign multiple variables at the same time in one line of code.
```python
name, age, attractive= "Bro", 32, True
print(name, age, attractive)
```
> in case different variables hold same value
```python
Bill = Tina = Steve = 30
print(Bill)
```
## 04. string methods 
- some functions we can use with strings
```python
print(name.find("B"))
print(name.capitalize())
print(name.upper())
print(name.lower())
print(name.isdigit())
print(name.isalpha())
print(name.count("o")) 
print(name.replace("o", 'a'))
print(name*3)
```
## 05. type cast
- **type casting** is converting the data type of a value to another data type.
```python
x = 1     #int
y = 2.0   #float
z = "3"   #str

# convert to string
x = str(x) 
y = str(y)
z = str(z)
# convert to float
x = float(x)
y = float(y)
z = float(z)
# convert to integer
x = int(x)
y = int(y)
z = int(z)
```
## 06. user input
```python
name = input("What is your name?: ")
age = int(input("How old are you?: "))
height = float(input("How tall are you?: "))

print("Hello "+name)
print("You are "+str(age)+ " years old")
print("You are "+str(height)+ " cm tall")
```
> we've converted the age into integer data type when entering it but we had to convert it back to string to display it

## 07. math functions
```python
import math

pi = 3.14
x = 1
y = 2
z = 3

print(round(pi))
print(math.ceil(pi))
print(math.floor(pi))
print(abs(pi)) # absolute value
print(pow(pi, 2)) # power function
print(math.sqrt(pi)) # square root
print(max(pi,x,y,z)) # finds max value
print(min(pi,x,y,z)) # finds min value
```
## 08. string slicing
- **string slicing** is creating a *substring* by extracting elements from another string. **indexing[ ]** or **slice( )**
```python
# [start:stop:step]
# start index in inclusive. stop index is exclusive.
# step is how much the index increases. default is 1.
name = "Bro Code"
first_name = name[:3]
last_name = name[4:]
funky_name = name[::3]
reversed_name = name[::-1]
print(first_name)
print(last_name)
print(funky_name)

website1 = 'http://test.com'
website2 = 'http://google.com'
slice = slice(7,-4)
print(website1[slice])
print(website2[slice])
```
## 09. if statements
- a block of code that will execute if its condition is **true**.
```python
age = int(input("How old are you?:"))

if age == 100:
    print("You are a century old!")
elif age >= 18:
    print("You are an adult!")
elif age <0:
    print("You have not been born yet!")
else:
    print("You are a child!")
```
## 10. logical operators
- the logical operators ( **AND** , **OR** , **NOT** ) are used to check if two or more conditional statements are true.
```python
temp = int(input("What is the temperature ourside?: "))

if (temp >= 0 and temp <= 30):
    print("The weather is good today!")
    print("Go outside!")
elif (temp <0 or temp >30):
    print("The weather is bad today!")
    print("Stay inside!")

# the NOT operator inverts the statement
if not(temp >= 0 and temp <= 30):
    print("The weather is bad today!")
    print("Stay inside!")
elif not(temp <0 or temp >30):
    print("The weather is good today!")
    print("Go outside!")
```
## 11. while loops

- a **while** loop is a statement that will execute its block of code as long as its condition is true

```python
name = ""
while len(name) == 0: # we can also write "while not name:"
    name = input("Enter your name: ")
print("Hello "+name)
```
## 12. for loops
- a **for** loop is a statement that will execute its block of code a limited amount of times
``` python
for i in range(10):
    print(i)
```
- **countdown timer**
```python
import time

for seconds in range(10,0,-1):
    print(seconds)
    time.sleep(1)
print("Happy New Year!")
```

## 13. nested loops
```python
rows = int(input("How many rows?: "))
columns = int(input("How many columns?: "))
symbol = input("Enter a symbol to use: ")

for i in range(rows):
    for j in range(columns):
        print(symbol, end="") # to avoid making a new line
    print()
```

## 14. loop control statements
- used to *change* a loop's execution from its normal sequence
```python
# break = used to terminate the loop entirely
# continue = skips to the next iteration of the loop
# pass = does nothing, acts as a placeholder

while True:
    name = input("Enter your name: ")
    if name !="":
        break

phone_number = "123-456-7890"
for i in phone_number:
    if i == "-":
        continue
    print(i, end="")

for i in range(1,21):
    if i == 13:
        pass
    else: print(i)
```

## 15. lists
- **lists** are used to store multiple items in a single variable
```python
food = ["pizza", "hamburger", "hotdog"]

food.append("ice cream")
food.remove("hotdog")
food.pop() #removes last element in list
food.insert(0,"cake")
food.sort()
food.clear()

print(food[0])

for x in food:
    print(x)
```

## 16. 2D lists
- a **2D list** is basically a list of lists

```python
drinks = ["coffee", "soda", "tea"]
dinner = ["pizza", "hamburger", "hotdog"]
desert = ["cake", "ice cream"]

food = [drinks, dinner, desert]
print(food[0][1])
print(food[1][1])
```

## 17. tuples
- a **tuple** is a collection which is ordered and unchangeable, it's used to group together related data
```python
student = ("Bro", 21, "male")
print(student.count("Bro")) 
print(student.index("male"))

for x in student:
    print(x)

if "Bro" in student:
    print("Bro is here!")
```

## 18. sets
- a **set** is a collection which is unordered, unindexed and doesn't include duplicare values

```python
utensils = {"fork", "spoon", "knife"}
dishes = {"bowl", "plate", "cup", "knife"}

utensils.add("napkin")
utensils.remove("fork")
utensils.clear()
dishes.update(utensils)
dinner_table = utensils.union(dishes)

print(dishes.difference(utensils))
print(utensils.intersection(dishes))

for x in dinner_table:
    print(x)
```
## 19. dictionaries
- a **dictionary** is a changeable, unordered collection of unique *key:value* pairs. dictionaries are fast because they use hashing, which allows us to access a value quickly!

```python
capitals = {'USA':'Washington DC',
            'India':'New Dehli',
            'China': 'Beijing',
            'Russia': 'Moscow'}
print(capitals['Russia']) #this causes issues if not in dictionary. Get method better.
print(capitals.get('Germany')) # this will return None if not there.
print(capitals.keys()) # will print only the keys
print(capitals.values()) # will print only the values
print(capitals.items()) # will print all items

for key, value in capitals.items(): # this will also print whole dictionary.
    print(key, value)

capitals.update({'Germany': 'Berlin'}) # way to add to dictionary.
capitals.update({'USA': 'Las Vegas'}) # way to update or add to dictionary.
capitals.pop('China') # removes key, value from dictionary.
capitals.clear()
```

## 20. indexing
- the **index operator** ```[]``` gives us access to a sequence's element (ex. strings, lists, tuples..)

```python
name = "bro Code!"
if(name[0].islower()):
    name = name.capitalize()
print(name)

first_name = name[:3].upper()
last_name = name[4:].lower()
last_character = name[-1]

print(first_name)
print(last_name)
print(last_character)
```

## 21. functions!
- a **function** is a block of code that is executed only when it is called

```python
def hello(first_name, last_name, age): # parameters
    print("Hello "+first_name+" "+last_name)
    print("You are "+ str(age) + " years old") # we need to convert it to string
    print("Have a nice day!")

hello("Bro", "Code", 21) # arguments
```
## 22. return statement
- the **return** value is the value or object that a function sends back to the caller

```python
def multiply(number1, number2):
    return number1 * number2 # the result

x = multiply(6,8)
print(x)
```
## 23. keyword arguments
- arguments preceded by an identifier when passed to a function are known as **keyword arguments**; unlike positional arguments, their order does *not* matter, as python knows the names of the arguments that the function receives

```python
def hello(first,middle,last):
    print("Hello "+first+" "+middle+" "+last)

hello("Code", "Dude", "Bro") # positional arguments.
hello(last="Code", middle="Dude", first="Bro") # keyword arguments.
```
## 24. nested function calls
- **nested function calls** are when one function call is used as an argument for another function. these calls are resolved from the innermost to the outermost, with the return value of the inner function serving as the argument for the next outer function

```python
num = input("Enter a whole positive number: ")
print(num)
num = float(num)
print(num)
num = abs(num)
print(num)
num = round(num)
print(num)
# we can simplify all this using a nested function call
print(round(abs(float(input("Enter a whole positive number: ")))))
```
## 25.