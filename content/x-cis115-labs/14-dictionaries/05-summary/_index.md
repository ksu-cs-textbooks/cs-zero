---
title: "Summary"
pre: "5. "
weight: 50
date: 2021-04-23T00:00:01-05:00
---

In this lab, we introduced several major important topics in Python. Let's quickly review them.

## Python Dictionaries

Dictionaries in Python allow us to store **key-value** pairs in a single data structure. **Keys** are used to uniquely identify an associated **value**. 

Dictionaries can be created using curly brackets `{}`:

```python
dict_1 = {}
dict_2 = {"a": 1, "b": 2, "c": 3}
```

## Adding and Accessing Dictionary Items

New elements can be added to a dictionary by providing a new key in square brackets:

```python
dict_2 = {"a": 1, "b": 2, "c": 3}
dict_2["d"] = 4
```

Items can also be accessed and updated using square brackets

```python
dict_2 = {"a": 1, "b": 2, "c": 3}
dict_2["c"] = dict_2["a"] + dict_2["b"]
```

## Loops with Dictionaries

Dictionaries can be iterated by just the keys or by the keys and values in a tuple:

```python
dict_3 = {
    "cat": "mammal",
    "lizard": "reptile",
    "goldfish": "fish",
    "chickadee": "bird"
}

# keys only
for key in dict_3:
    print("{}: {}".format(key, dict_3[key]))

# keys and values
for key, value in dict_3.items():
    print("{}: {}".format(key, value))
```

## Functions with Dictionaries

When calling a function that accepts a dictionary as a parameter, the argument is passed using **call by reference** instead of **call by value**. The original dictionary can be modified by the function, but it cannot be replaced with a new dictionary unless the reference to that new dictionary is returned from the function.