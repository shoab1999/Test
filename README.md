# Python

- [Python](#python)
  - [Variables](#variables)
    - [Multiple assignment](#multiple-assignment)
  - [Convertring Number to String](#convertring-number-to-string)
  - [Concatanation](#concatanation)
  - [string formating](#string-formating)
    - [string method](#string-method)
  - [Function](#function)
    - [return](#return)
    - [lambda function](#lambda-function)
  - [List](#list)
    - [create list](#create-list)
  - [tuple](#tuple)
  - [Dictionary](#dictionary)
  - [Condition](#condition)
    - [Nested If](#nested-if)
    - [logical operator](#logical-operator)
    - [membership operator](#membership-operator)
  - [loop](#loop)
    - [range](#range)
      - [ex:](#ex)

jupyter nbconvert --to markdown crash_course.ipynb --output README.md


## Variables

- Variable names are case sensitive(name and NAME are different variables)
- Must start with a letter or an underscore
- can have numbers but can not start with one


```python
x = 1          # int
y = 1.234      #float
name = 'Shoab'  #str
is_admin= True
print(x)
print(y)
print(name)

if is_admin:
    print("allow")
else:
    print("not allowed")

lover = False

if not lover: # !0 =1
    print("Not a lover")

```

    1
    1.234
    Shoab
    allow
    Not a lover
    

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

    <class 'float'> 1.0
    

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
    

### string method



```python
s='hello world'
print(s.capitalize( ))
print(s.endswith('d' ))
print(s.split( ))
print("81/1,aruapara,kushtia".split(","))
print(s.find('r'))
print(s.upper( ))


```

    Hello world
    True
    ['hello', 'world']
    ['81/1', 'aruapara', 'kushtia']
    8
    HELLO WORLD
    

## Function




```python
print("Outside of function printInfo ")
def printInfo():
    print("Inside of function printInfo ") 
    print("Inside of function printInfo ")  
    if 10>3:
        print("still inside")
print("Outside of function printInfo ")


print("Outside of function printInfo ")



```

    Outside of function printInfo 
    Outside of function printInfo 
    Outside of function printInfo 
    


```python
printInfo()
```

    Inside of function printInfo 
    Inside of function printInfo 
    still inside
    

### return


```python
def printInfo(n):
    return n**2
```


```python
sqr = printInfo(4)
print(sqr)

```

    16
    

### lambda function

def


```python
# def getSum(num1, num2):
#     total= num1+num2
#     return total
# or
# # def getSum(num1, num2): return num1+num2
getSum = lambda num1,num2 : num1+num2

```


```python
print(getSum(1,2))
```

    3
    

## List

### create list


```python
numbers = [1,2,3,4,5]
fruits = ['Apples', 'Oranges', 'Graps']
#access
print(fruits[0])
#finding length
print(len(fruits))
#add
fruits.append('mangoes')
print(fruits)
#remove
fruits.remove('Graps')
print(fruits)
#insert(i,el)- add an element at position `i`
fruits.insert(1, 'Strawberries')
print(fruits)
fruits[1] = 'banna'
print(fruits)

#remove with pop
fruits.pop(2)
#reverse list
fruits.reverse()
print(fruits)

#sort list
fruits.sort()
print(fruits)
```

    Apples
    3
    ['Apples', 'Oranges', 'Graps', 'mangoes']
    ['Apples', 'Oranges', 'mangoes']
    ['Apples', 'Strawberries', 'Oranges', 'mangoes']
    ['Apples', 'banna', 'Oranges', 'mangoes']
    ['mangoes', 'banna', 'Apples']
    ['Apples', 'banna', 'mangoes']
    

## tuple


```python
#create tuple
fruits=('Apples', 'Oranges','Grapes' )

print(fruits)
print(fruits[1])
```

    ('Apples', 'Oranges', 'Grapes')
    Oranges
    


```python
# unlke list tuple is not changeable
fruits[1] = 'banna'
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    C:\Users\MDSHOA~1\AppData\Local\Temp/ipykernel_12496/2254711348.py in <module>
          1 # not changeable
    ----> 2 fruits[1] = 'banna'
    

    TypeError: 'tuple' object does not support item assignment


## Dictionary


```python
# storing student info in a list
student= ['Shoab', 191902039, 'PC-191']
# access  using `index` position
print(student)
print(student[0])
print(student[1])
# vs 
# in a dictionary:
student = {
    'name' : "soab",
    'id':191902061,
    'batch':'PC-191'
}
# access using `key`
print()
print(student)
print(student['name'])
print(student['id'])
```

    ['Shoab', 191902039, 'PC-191']
    Shoab
    191902039
    
    {'name': 'soab', 'id': 191902061, 'batch': 'PC-191'}
    soab
    191902061
    


```python
# error 
print(student['age'])
```


    ---------------------------------------------------------------------------

    KeyError                                  Traceback (most recent call last)

    C:\Users\MDSHOA~1\AppData\Local\Temp/ipykernel_7884/2291910217.py in <module>
          1 # error
    ----> 2 print(student['age'])
    

    KeyError: 'age'



```python
# no error with get method
print(student.get('age'))
```

    None
    


```python
# change the value
student['id']= 191902039
print(student)
```

    {'name': 'soab', 'id': 191902039, 'batch': 'PC-191'}
    


```python
#add key value
student['phone']= 17665530356
print(student)
```

    {'name': 'soab', 'id': 191902039, 'batch': 'PC-191', 'phone': 17665530356}
    


```python
#get dic keys
print(student.keys())

```

    dict_keys(['name', 'id', 'batch', 'phone'])
    


```python
#get items
# print(student.items()) # dict_items([('name', 'soab'), ('id', 191902061), ('batch', 'PC-191')])

for k, v in student.items():
    print(k+" : "+str(v))
```

    name : soab
    id : 191902039
    batch : PC-191
    phone : 17665530356
    


```python
#remove
del(student['phone'])
#pop
# student.pop('phone')
print(student)
```

    {'name': 'soab', 'id': 191902039, 'batch': 'PC-191'}
    


```python
# list of dic?
student=[
    {'name': 'Shoab', 'id': 39},
    {'name' :'Sarukh', 'id':61},
    {'name': 'Bappy', 'id': 43}
    ]
print(student)
```

    [{'name': 'Shoab', 'id': 39}, {'name': 'Sarukh', 'id': 61}, {'name': 'Bappy', 'id': 43}]
    


```python
print(student[1])
print(student[1]['name'])
```

    {'name': 'Sarukh', 'id': 61}
    Sarukh
    

## Condition


```python
x=12
y=10
if x>y:
    print(f'{x} is greater than {y}')



```

    12 is greater than 10
    


```python
x=12
y=12
if x>y:
     print(f'{x} is greater than {y}')
else:
     print(f'{y} is greater than {x}')
```

    12 is greater than 12
    


```python
# elif
if x> y:
   print(f'{x} is greater than {y} ')
elif x==y:
    print(f'{x} is equal to {y}')
else:
    print(f'{y} is greater than {x}')
```

    12 is equal to 12
    

### Nested If


```python
x=5
if x>2:
    if x<=10:
        print(f'{x} is greater than 2 and less than or equal to 10')

```

    5 is greater than 2 and less than or equal to 10
    

### logical operator



```python
if x>2 and x<=10:
    print(f'{x} is greater than 2 and less than or equal to 10')
```

    5 is greater than 2 and less than or equal to 10
    

### membership operator


```python
x=39
lists = [1,2,3,4,9,8]
if x in lists:
    print(x)
else:
    print('not found')

```

    not found
    


```python
x=39
lists = [1,2,3,4,9,8]
if x not in lists:
    print('not found')
```

    not found
    

## loop


```python
people=['maria','shoab','bappy']
for person in people:
    print(f'Current person: {person}')

```

    Current person: maria
    Current person: shoab
    Current person: bappy
    


```python

#break
for person in people:
    if person == 'maria':
        print (f'Current Person : {person}')
        break

```

    Current Person : maria
    


```python
#continue === skip
for person in people:
    if person == 'maria':
        continue
    print (f'Current Person : {person}')
```

    Current Person : shoab
    Current Person : bappy
    

### range


```python
for x in range(1,5):
    print(x)
```

    1
    2
    3
    4
    


```python
# how to get index of maria?????
people=['A','shoab','bappy','maria']
i = 0;
for person in people:
    if person == 'maria':
        print(i)
        break
    i = i + 1

print(people[i])
```

    3
    maria
    


```python
for i in range(len(people)):
    if people[i] == 'maria':
       print(i)
```

    3
    

#### ex:


```python
Result=[{
'Semi': 191, 'CH': 9, 'GPA': 3.75, 'CGPA': 3.75
},
{
'Semi': 191, 'CH': 9, 'GPA': 3.75, 'CGPA': 3.75
},
{
'Semi': 191, 'CH': 9, 'GPA': 3.75, 'CGPA': 3.75
},
{
'Semi': 191, 'CH': 9, 'GPA': 3.75, 'CGPA': 3.75
},
]

for r in Result:
    print(f"Semester: {r['Semi']}, Credi: {r['CH']}, GPA: {r['GPA']},CGPA: {r['CGPA']}")

```

    Semester: 191, Credi: 9, GPA: 3.75,CGPA: 3.75
    Semester: 191, Credi: 9, GPA: 3.75,CGPA: 3.75
    Semester: 191, Credi: 9, GPA: 3.75,CGPA: 3.75
    Semester: 191, Credi: 9, GPA: 3.75,CGPA: 3.75
    


```python
import requests
import json

```


```python
url = 'https://reqres.in/api/users?page=2'
res = requests.get(url)
res = json.loads(res.text)
res
```




    {'page': 2,
     'per_page': 6,
     'total': 12,
     'total_pages': 2,
     'data': [{'id': 7,
       'email': 'michael.lawson@reqres.in',
       'first_name': 'Michael',
       'last_name': 'Lawson',
       'avatar': 'https://reqres.in/img/faces/7-image.jpg'},
      {'id': 8,
       'email': 'lindsay.ferguson@reqres.in',
       'first_name': 'Lindsay',
       'last_name': 'Ferguson',
       'avatar': 'https://reqres.in/img/faces/8-image.jpg'},
      {'id': 9,
       'email': 'tobias.funke@reqres.in',
       'first_name': 'Tobias',
       'last_name': 'Funke',
       'avatar': 'https://reqres.in/img/faces/9-image.jpg'},
      {'id': 10,
       'email': 'byron.fields@reqres.in',
       'first_name': 'Byron',
       'last_name': 'Fields',
       'avatar': 'https://reqres.in/img/faces/10-image.jpg'},
      {'id': 11,
       'email': 'george.edwards@reqres.in',
       'first_name': 'George',
       'last_name': 'Edwards',
       'avatar': 'https://reqres.in/img/faces/11-image.jpg'},
      {'id': 12,
       'email': 'rachel.howell@reqres.in',
       'first_name': 'Rachel',
       'last_name': 'Howell',
       'avatar': 'https://reqres.in/img/faces/12-image.jpg'}],
     'support': {'url': 'https://reqres.in/#support-heading',
      'text': 'To keep ReqRes free, contributions towards server costs are appreciated!'}}




```python

list_of_user = res['data']
for user in list_of_user:
    email = user['email']
    firstName = user['first_name']

    print(f"Email: {email}, Name: {firstName} ")
```

    Email: michael.lawson@reqres.in, Name: Michael 
    Email: lindsay.ferguson@reqres.in, Name: Lindsay 
    Email: tobias.funke@reqres.in, Name: Tobias 
    Email: byron.fields@reqres.in, Name: Byron 
    Email: george.edwards@reqres.in, Name: George 
    Email: rachel.howell@reqres.in, Name: Rachel 
    
