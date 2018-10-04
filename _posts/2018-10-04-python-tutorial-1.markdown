---
layout: post
title:  "Python Tutorial #1"
date:   2018-10-04 19:35:42 +0200
categories: python tutorial
---

Topics for today:

1. What is variable?
2. What can variable contain?
3. Operations with variables
4. Complex variables types
5. User input
6. Conditions

## Before we start

My lectures are based on practice in incremental steps. Practice, practice, practice...

Follow this preparation steps:
1. Register on [https://repl.it/](https://repl.it/)
2. Create new Python 3 repl, you should see your screen divided into 3 blocks:  
   Files tree, text editor and black console
3. Copy and paste this code: `print("Hello World")` and push `run` button.  
   You should see that "Hello World" appears in console, like this:

![Hello World](/assets/hello_world.png)
   

## What is variable?

Did you ever used spreadsheet in Excel or Google? Guess what, you already know what variable is.  
Variable is one cell in table, which is described by cell name and can contain some value.

|   |      A          |   B        |
|---|:---------------:|:----------:|
| 1 |  my             | 1          |
| 2 |  True           | 3.14       |


What are variables in the table above?

1. A1 with value **my**
2. A2 with value **True**
3. B1 with value **1**
4. B2 with value **3.14**

In other words, variable is a box with name, which is contain some value. We usually use variables to store information for future use.

Now we need to learn how to define variable in Python.

```python
# you did't expect this will be so easy, did you?
a1 = "my"
a2 = True
b1 = 1
b2 = 3.14
```

Define variable in Python has it's own rules. It is always an expression like:

```python
variable_name = value
```

So on the left side of `=` sign we have variable's name and on the right side is always variable's value.

Also we have some style rules which we **must** follow when defining a new variable:

1. Name of your variable is really important, and must describe value that variable contain:

   ```python
   first_name = "alfredo"
   # vs
   xyz = "alfredo"
   ```
2. Variable name should always be in lower case:

   `a1` or `a2` or `username`
3. When variables contain more then one word, separate them with `_`:

   `first_name` or `flight_number` or `you_name_it`

## What can variable contain?

Type of value that variable contain is describing variable itself.  
So for example if variable named `first_name` contain a string, you can call it a string variable.  
Now I will explain you 3 basic variable types to understand concepts of operations with them.

### Numbers - Integers and Floats

As you already noticed, variables can contain numbers.  
Numbers like `1`, `2`, `100`, `-1` are called `integers` and they represent whole numbers.  
Numbers like `3.14` are called `float` and they represent real numbers.

```python
# age and weight are integer variables
age = 18
weight = 75
# price is float variable
price = 100.14
```

### Strings or Text

Strings in Python are represented as text surrounded by double quotes:

```python
first_name = "vladimir"
username = "moonchel"
reservation_number = "ABC123"
```

### Boolean

Boolean value is describing only two states: `on` or `off`.  
In Python for `on` we use `True` and for `off` we use `False`.

```python
switch_state = True
is_turned_on = False
reservation_is_paid = True
```

## Operations with variables

Now when we know what variable is and how to define them, let's see an example of variable operations:

```python
a = 1
b = 2
c = a + b
print(c)
```

What do you expect `c` variable will contain? Copy and paste this code and run it.  
Yes, it's quite logical that `c` contains `3` as it's value.  
Here are few more examples:

```python
# convert miles to kilometers
miles = 10
kilometers = miles * 1.60934
print(miles, 'mi(s)', 'is equal to', kilometers, 'km(s)')

# calculate circle area
r = 15
pi = 3.14
circle_area = pi * r * r
print(circle_area)
```

### 🚀 What time is it? It's TASKs time. 🚀

In the same way as to examples above:

1. Write a program that will convert 12 pounds to kilograms
   <details>
    <summary>Answer</summary>
    <p>
    ```python
    pounds = 12
    kilograms = pounds * 0.453592
    print(pounds, 'lb(s)', 'is equal to', kilograms, 'kg(s)')    
    ```
    </p>
   </details>

2. Write a program that will convert 156 CZK to EUR

