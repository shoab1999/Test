# Python

- [Python](#python)
  - [Variables](#variables)
    - [Multiple assignment](#multiple-assignment)
  - [Convertring Number to String](#convertring-number-to-string)
  - [Concatanation](#concatanation)
  - [string formating](#string-formating)
  - [Function](#function)
  - [create list](#create-list)


jupyter nbconvert --to markdown crash_course.ipynb --output README.md


## Variables

- Variable names are case sensitive(name and NAME are different variables)
- Must start with a letter or an underscore
- can have numbers but can not start with one


```python
x = 1          # int
y = 1.234      #float
name = 'Shoab'  #str
is_cool= True
print(x)
print(y)


```

    1
    1.234
    

### Multiple assignment


```python
x, y, name, is_cool= (1, 2.5, 'john', True)
print(x, y, name, is_cool, )
```

    1 2.5 john True
    

## Convertring Number to String

- `str()` : to convert to `String`
- `int()` : to convert to `integer` 
- `type()` : to check data type


```python
x = str(x)
y = int(y)
z = float(y)
print(type(z), z)
```

    <class 'float'> 2.0
    

## Concatanation


```python
id =191
print("Hello "+str(id)+"")
print(f"ID: {id}")


```

    Hello 191
    ID: 191
    

## string formating


```python
name = 'Brad'
age = 37
print('My name is {name} and I am {age}'.format (name=name, age=age))
```

    My name is Brad and I am 37
    

###string method



```python
s='hello world'
print(s.capitalize( ))
print(s.endswith('d' ))
print(s.split( ))
print(s.find('r'))
print(s.upper( ))


```

    Hello world
    True
    ['hello', 'world']
    8
    HELLO WORLD
    

## Function




```python
def printInfo(n):
    return n**2

print("Outside")
```

    Outside
    


```python
sqr = printInfo(4)
print(sqr)
```

    16
    

## create list


```python
numbers = [1,2,3,4,5]
fruits = ['Apples', 'Oranges', 'Graps']
print(fruits[1])
print(len(fruits))

```

    Oranges
    3
    


```python

```
