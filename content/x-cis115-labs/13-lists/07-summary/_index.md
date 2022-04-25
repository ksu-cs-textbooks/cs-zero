---
title: "Summary"
pre: "7. "
weight: 70
date: 2021-04-10T00:00:01-05:00
---

In this lab, we introduced several major important topics in Python. Let's quickly review them.

## Python Lists

Lists in Python allow us to store multiple **elements** in a single variable, with each element identified by a unique **index** within the list.

Lists can be created using square brackets `[]`:

```python
list_a = []
list_b = [5, 3, 7]
```

## Adding and Accessing List Items

New elements can be added to a list using the `append()` method:

```python
list_a = []
list_a.append(4)
```

Items in a list can be accessed and updated using square brackets:

```python
list_b = [5, 3, 7]
list_b[2] = list_b[0] + list_b[1]
```

## Loops with Lists

Lists can be iterated using both for loops and while loops:

```python
list_b = [5, 3, 7]

for i in list_b:
    print(i)

j = 0
while j < len(list_b)
    print(list_b[j])
    j = j + 1
```

Lists should not be changed while iterating using a for loop. 

## Functions with Lists

When calling a function that accepts a list as a parameter, the argument is passed using **call by reference** instead of **call by value**. The original list can be modified by the function, but it cannot be replaced with a new list unless the reference to that new list is returned from the function.

## Strings as Lists

Strings can be iterated just like a list, and we can use square brackets to access individual characters in a string. However, lists are still passed as **call by value** when provided as an argument to a function.

## Slicing

We can create a **slice** of a list by specifying a `start`, `end` and `step` value separated by colons. The values may be omitted, and may also be negative.

```python
list_b = [5, 3, 7]
print(list_b[-1])
print(list_b[0:1])
print(list_b[0:2:2])
print(list_b[::-1])
```
