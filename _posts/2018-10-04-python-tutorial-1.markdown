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
   1. [Dictionaries](#dictionaries)
   2. [Lists](#lists)
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

Here is a set of all possible operations with numbers in Python:

```python
print(2 + 3)  # 5
print(4 - 3)  # 1
print(5 / 2)  # 2.5
print(5 * 2)  # 10
print(5 ** 2) # 25 - square
print(5 // 3) # 1 - floor division, try it if you don't understand
print(5 % 3)  # 2 - remaining from division
```

### Strings ##

Strings in Python are represented as text surrounded by double quotes:

```python
first_name = "vladimir"
username = "moonchel"
reservation_number = "ABC123"
```

Here is a subset of all possible operations with text:

```python
text_1 = "Lorem ipsum"
text_2 = "dolor sit amet"

print(text_1 + " " + text_2)

```

### Booleans ##

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


### Text

For now I will show only `+` operator. How we can add 2 or more strings, you can ask? We can join them...

```python
# Hello world - this operation is called concatenation
print("Hello" + " " + "World")
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


## Complex variables types ##

### Dictionaries ##

Imagine you often need to translate country name to its abbreviation.  
So you will create a table like this:

|   |  country name   |  abbreviation  |
|---|:---------------:|:--------------:|
| 1 |  Belgium        | BE             |
| 2 |  Greece         | EL             |
| 3 |  Portugal       | PT             |

And then use `Find` command to find abbreviation for some country name.  
This can be described in Python via dictionaries:

```python
countries_abbs = {
  "Belgium": "BE",
  "Greece": "EL",
  "Portugal": "PT",
}

print(countries_abbs["Belgium"])  # will print "BE"
print(countries_abbs["Portugal"]) # will print "PT"
```

Dictionaries can be used as translation table, another example can be fruit price table:

```python
fruits_prices = {
   "apple": 10,
   "pear": 12,
   "banana": 13
}

# cost for 2 apples and 3 pears and 1 banana
cost = 2 * fruits_prices["apple"] + 3 * fruits_prices["pear"] + fruits_prices["banana"]

print(cost) # what result will be here?
```

Dictionaries definition has it's own format:
1. `{}` - this means you defined empty dictionary. 
2. `{ 'apple': 10, }` - means that your dictionary contains 1 `key: value` (read key-value) pair.

So, please remember format: **figure brackets with key-value pairs separated by comma**.  
P.S. Notice last comma and don't remember to put it after last key-value pair.

### Lists ##

Imagine you have a list of car prices and need to sum them up in this kind of table:

|     |  price   |
|-----|:--------:|
| 1   |  10      |
| 2   |  11      |
| 3   |  9       |
| SUM |  30      |

How this can be described in Python?

```python
prices = [10, 11, 9]

prices_sum = prices[0] + prices[1] + prices[2]

print(prices_sum) # what result will be here?
```

As you can see lists represents group of values.  
Lists has there own definition format:
1. `[]` - this means you defined an empty list
2. `[1, 2, 3,]` - this means you defined a list that contains 3 numbers

To access an element in a list you have to use `indexing`. You need to know the index of value.  
**Indexes in Python are starting from 0**. So for example `prices[0]` is equal to `10`.


### 🚀 What time is it? It's TASKs time. 🚀

<details>
<summary>
Transform this table to Python dictionary and try to use it:

<table>
   <thead>
      <tr>
         <th>IATA code</th>
         <th>Airport name</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td>TIA</td>
         <td>Tirana Airport</td>
      </tr>
      <tr>
         <td>EVN</td>
         <td>Yerevan Zvartnots Airport</td>
      </tr>
      <tr>
         <td>GRZ</td>
         <td>Graz Airport</td>
      </tr>
      <tr>
         <td>INN</td>
         <td>Innsbruck Airport</td>
      </tr>
   </tbody>
</table>
</summary>
<pre>
airports_names = {
   'TIA': 'Tirana Airport',
   'EVN': 'Yerevan Zvartnots Airport',
   'GRZ': 'Graz Airport',
   'INN': 'Innsbruck Airport',
}

print('These airports', airports_names['TIA'], airports_names['GRZ'], 'are cool!')
</pre>
</details>

<details>
<summary>
Calculate mean for avocado prices in different states.  
Your input prices list is: [10, 12, 9, 16]
</summary>
<pre>
avocado_prices = [10, 12, 9, 16]
avocado_prices_sum = costs[0] + costs[1] + costs[2] + costs[3]
avocado_prices_mean = avocado_prices_sum / 4
print('Mean for avocado prices is:', avocado_prices_mean)
</pre>
</details>


## User input ##

How we can ask user for his name or age? Like this:

```python
name = input("Hi, what is your name?")
age = int(input("Hi " + name + ", how old are you?"))
```

For getting user input from keyboard you need to use `input` function.  
Inside of it, you *can* define a string, which will tell user what kind of information you want to know.

*Here we store variables for future use. We use `name` variable when asking about age.*

Last thing we need to know, the result of `input` function is always a **string**.  
To transform it to integer or float use `int` or `float` functions.


### 🚀 What time is it? It's TASKs time. 🚀

<details>
<summary>
Write a program for converting miles to km, and on start asks user to input miles. Print the result.
</summary>
<pre>
miles = int(input('Miles:'))
kilometers = miles * 1.60934
print(kilometers)
</pre>
</details>

<details>
<summary>
Ask user for 3 numbers and sum them. Print the result.
</summary>
<pre>
number_1 = int(input('1 num:'))
number_2 = int(input('2 num:'))
number_3 = int(input('3 num:'))

numbers_sum = number_1 + number_2 + number_3
print(numbers_sum)
</pre>
</details>

<details>
<summary>
   Character input - 
   <a href="https://www.practicepython.org/exercise/2014/01/29/01-character-input.html" target="_blank">
      Task details
   </a> 
</summary>
</details>


## Conditions

How we can control flow of our program? Image you are working at the store, and someone wants to buy alcohol.  
You will ask them: "How old are you?", and they will respond with some number, hopefully greater then 17.  
Based on this number you will decide what to do: sell or not to sell. How this can be described in Python?


```python
age = int(input("How old are you?"))

if age > 17:
   print("Cool enough")
else:
   print("Nope, sorry bro")
```

This called a `condition` statement and has it's own definition format:
1. Started with `if` word and then a `condition` which must be evaluated to `True` or `False` and **colon**.
2. Body of `if` when condition is `True`. Please notice that body must be intended to 2 or 4 spaces. 
   P.S. For `repl.it` by default it is 2 spaces or 1 tab.
3. `else` with a colon.
4. Body of else statement. This part and `else:` is not necessary to have. You can have only `if` and body for it.

Other example:

```python
# double equal sign mean you want to check if what on the left is equal to what on the right
# so in our case if user will check if user input is equal to yes
weather_is_rainy = input("Is it rainy out there?") == "yes"

if weather_is_rainy == True:
  print('Take an umbrella')
else:
  print('Don\'t need to')
```

### 🚀 What time is it? It's TASKs time. 🚀

<details>
<summary>
   Odd or even - 
   <a href="https://www.practicepython.org/exercise/2014/02/05/02-odd-or-even.html" target="_blank">
      Task details
   </a> 
</summary>
</details>

