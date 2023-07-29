---
title: "Data Structure/ Ch01:BasicPython"
layout: single
typora-root-url: ../
categories: DataStructure
tag: [python, algorithm, datastructure]
toc: true
---



# Python Basic Review

Practiced below codes for recalling



```python
range(10)
```


    range(0, 10)


```python
list(range(10))
```


    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]


```python
list(range(1,10,2))
```


    [1, 3, 5, 7, 9]


```python
list(range(10,1,-1))
```


    [10, 9, 8, 7, 6, 5, 4, 3, 2]


```python
"David"
```


    'David'


```python
myName = "David"
```


```python
print(myName)
```

    David

```python
myName.upper()
```


    'DAVID'


```python
myName.center(10)
```


    '  David   '


```python
myName.find('v')
```


    2


```python
myName.split('v')
```


    ['Da', 'id']





##  Practice- Making a simple calculator / Function


```python
def cal_upper(price):
    increment = price*0.3
    upper_price = price + increment
    return upper_price
```


```python
cal_upper(13000)
```


    16900.0




```python
def cal_upper_lower(price):
    offset = price * 0.3
    upper = price + offset
    lower = price - offset
    return (upper, lower)
```


```python
cal_upper_lower(1200)
```


    (1560.0, 840.0)




```python
for i, stock in enumerate(['ABC', 'DEF', 'GHI']):
    print(i, stock)
    # return the result with index
```

    0 ABC
    1 DEF
    2 GHI



```python
def myaverage(a, b):
    return a+b//2

myaverage(2,3)
```


    3


```python
def get_max_min(data_list):
    max_val = max(data_list)
    min_val = min(data_list)
    return (max_val, min_val)
```


```python
get_max_min([1,10])

```


    (10, 1)


```python
a=[range(1,19)]    # you can enter the integar only
get_max_min(a)
```


    (range(1, 19), range(1, 19))





## Practice - Making a BMI result categorizing / if & elif


```python
def bmiResult(weight, height):
    bmi = weight // height
    if bmi < 18.5:
        return "underweight"
    elif bmi >= 18.5 and bmi < 25.0:
        return "normal"
    elif bmi >= 25.0 and bmi < 30.0:
        return "overweight"
    else:
        return "obese"
```


```python
bmiResult(185, 88), bmiResult(185,99)
```


    ('underweight', 'underweight')



## Practice - Class 

Made a Fraction class for exe


```python
# Listing 1.9

def gcd(m,n):
    while m%n != 0:
        oldm = m
        oldn = n
        
        m - oldn
        n - oldm%oldn
    return n


class Fraction:
    def __init__(self, top, bottom):
        self.num = top
        self.den = bottom
        
    def __str__(self):
        return str(self.num)+"/"+str(self.den)
    
    def show(self):
        print(self.num, "/", self.den)
        
    def __add__(self, otherfraction):
        newnum = self.num*otherfraction.den + \
                    self.den*otherfraction.den
        newden = self.den * otherfraction.den
        common = gcd(newnum,newden)
        return Fraction(newnum//common, newden//common)
    
    def __eq__(self, other): 
        firstnum = self.num * other.den
        secondnum = other.num * self.den
        
        return firstnum == secondnum
```


```python
f1 = Fraction(1,4)
```


```python
f2 = Fraction(1,2)
```


```python
print(f1)
```

    1/4

```python
print(f2)
```

    1/2

```python
f3=f1+f2
```



## Summary

Summary
1. Lists, tuples, and strings are built in Python sequential collections.
2. Dictionaries and sets are nonsequential collections of data.
3. Classes allow programmers to implement abstract data types.
4. Programmers can override standard methods as well as create new methods.
5. Classes can be organized into hierachies

