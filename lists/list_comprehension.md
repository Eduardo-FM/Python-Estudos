# List Comprehension

List comprehension offers a shorter syntax when you want to create a new list based on the values of an existing list.

Example:

Based on a list of fruits, you want a new list, containing only the fruits with the letter "a" in the name.

Without list comprehension you will have to write a for statement with a conditional test inside:

```python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = []

for x in fruits:
  if "a" in x:
    newlist.append(x)

print(newlist)

# OUT 
['apple', 'banana', 'mango']
```

With list comprehension you can do all that with only one line of code:

```python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

newlist = [x for x in fruits if "a" in x]

print(newlist)

# OUT 
['apple', 'banana', 'mango']
```

## The Syntax

> newlist = [expression for item in iterable if condition == True]

The return value is a new list, leaving the old list unchanged.

## Condition
The condition is like a filter that only accepts the items that valuate to True.

```python
newlist = [x for x in fruits if x != "apple"]
```

The condition if x != "apple"  will return True for all elements other than "apple", making the new list contain all fruits except "apple".

The condition is optional and can be omitted:

```python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

newlist = [x for x in fruits]

print(newlist)

#OUT
['apple', 'banana', 'cherry', 'kiwi', 'mango']
```

## Iterable
The iterable can be any iterable object, like a list, tuple, set etc.

## Expression
The expression is the current item in the iteration, but it is also the outcome, which you can manipulate before it ends up like a list item in the new list:

```python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

newlist = [x.upper() for x in fruits]

print(newlist)

#OUT
['APPLE', 'BANANA', 'CHERRY', 'KIWI', 'MANGO']
```

You can set the outcome to whatever you like

The expression can also contain conditions, not like a filter, but as a way to manipulate the outcome:

```python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

newlist = [x if x != "banana" else "orange" for x in fruits]

print(newlist)

#OUT
['apple', 'orange', 'cherry', 'kiwi', 'mango']
```