With the while loop we can execute a set of statements as long as a condition is true.

```python
i = 1
while i < 6:
  print(i)
  i += 1
```

**Note: remember to increment i, or else the loop will continue forever.**


## The break Statement
With the break statement we can stop the loop even if the while condition is true:

```python
i = 1
while i < 6:
  print(i)
  if i == 3:
    break
  i += 1
```

## The continue Statement
With the continue statement we can stop the current iteration, and continue with the next:

```python
i = 0
while i < 6:
  i += 1
  if i == 3:
    continue
  print(i)
```

## The else Statement
With the else statement we can run a block of code once when the condition no longer is true:

```python
i = 1
while i < 6:
  print(i)
  i += 1
else:
  print("i is no longer less than 6")
```