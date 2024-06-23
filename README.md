 # brocode's python full course notes 🐍♥️
> these are my notes from BroCode's python course on youtube, formatted in markdown for readability. i'm creating these notes to refer back to them in the future, and they might also benefit others following the course. i may add a table of contents later. good luck to everyone!
 
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


