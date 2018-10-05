---
layout: post
title:  "Python Tutorial #1"
date:   2018-10-04 19:35:42 +0200
categories: python tutorial
---

## Before we start

My lectures are based on practice in incremental steps.  
Make you comfortable, coffee, tea, beer and practice, practice, practice...

Follow this preparation steps:
1. Register on [https://repl.it/](https://repl.it/)
2. Create new Python 3 repl, you should see your screen divided into 3 blocks:
   Files tree, text editor and black console
3. Copy and paste this code: `print("Hello World")` and push `run` button.
   You should see that "Hello World" appears in console, like this:

![Hello World](/assets/hello_world.png)


## Topics for today

1. [What is variable?](#what-is-variable)
2. [What can variable contain?](#what-can-variable-contain)
   1. [Integers and Floats](#integers-and-floats)
   2. [Strings](#strings)
   3. [Boolean](#boolean)
3. [Operations with variables](#operations-with-variables)
4. [Complex variables types](#complex-variables-types)
5. [User input](#user-input)
6. [Conditions](#conditions)


## What is variable? ##

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

In other words, variable is a box with name, and contains some value.  
We usually use variables to store information for future use.  

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
3. When variable's name contains more then one word, separate them with `_`:

   `first_name` or `flight_number` or `you_name_it`

## What can variable contain? ##

Type of value that variable contain is describing variable itself.
So for example if variable named `first_name` contain a string, you can call it a string variable.
Now I will explain you 3 basic variable types to understand concepts of operations with them.

### Integers and Floats ##

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

### Strings ##

Strings in Python are represented as text surrounded by double quotes:

```python
first_name = "vladimir"
username = "moonchel"
reservation_number = "ABC123"
```

### Boolean ##

Boolean value is describing only two states: `on` or `off`.
In Python for `on` we use `True` and for `off` we use `False`.

```python
switch_state = True
is_turned_on = False
reservation_is_paid = True
```

## Operations with variables ##

### Numbers

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

Other available operations:

```python
print(2 + 3)  # 5
print(4 - 3)  # 1
print(5 / 2)  # 2.5
print(5 * 2)  # 10
print(5 ** 2)   # 25 - square
print(5 // 3) # 1 - floor division, try it if you don't understand
print(5 % 3)  # 2 - remaining from division
```

### Text

For now I will show only `+` operator. How we can add 2 or more strings, you can ask? We can join them...

```python
print("Hello" + " " + "World") # Hello world - this operation is called concatenation, don't need to remember
```

### Boolean

With boolean operations we use special operators: `not`, `or`, `and`. Less words, more code:

```python
print(True and True)          # True
print(True or False)          # True
print(not True and not False) # False 
```

Still don't understand? Yep, it is quite normal, you haven't seen `Truth table` yet:

![Truth Table](/assets/truth_table.png)

Use this table to understand boolean operations, try to understand how this table works.  
P.S. Try to substitute `True` with `1`, `False` with `0`, `or` with `+`, `and` with `*`, maybe you will find out something interesting


### 🚀 What time is it? It's TASKs time. 🚀

In the same way as to examples above:

<details>
<summary>Write a program that will convert 12 pounds to kilograms</summary>
<pre>
pounds = 12
kilograms = pounds * 0.453592
print(pounds, 'lb(s)', 'is equal to', kilograms, 'kg(s)')
</pre>
</details>

<details>
<summary>Write a program that will convert 156 CZK to EUR</summary>
<pre>
amount_in_czk = 156
amount_in_eur = amount_in_czk / 25.68
print(amount_in_czk, 'CZK', 'is equal to', amount_in_eur, 'EUR')
</pre>
</details>



