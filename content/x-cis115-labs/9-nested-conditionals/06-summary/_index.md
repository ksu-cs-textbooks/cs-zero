---
title: "Summary"
pre: "6. "
weight: 60
date: 2021-03-16T00:00:01-05:00
---

In this lab, we introduced several major important topics in Python. Let's quickly review them.

## Mutually Exclusive

Conditional statements are **mutually exclusive** when only one of the many branches will be executed for any possible input.

## Chained Conditionals

```python
if condition_1:
    print("1")
else
    if condition_2:
        print("2")
    else:
        if condition_3:
            print("3")
        else:
            print("4")
```

is equivalent to:

```python
if condition_1:
    print("1")
elif condition_2:
    print("2")
elif condition_3:
    print("3")
else:
    print("4")
```

## Nested Conditionals

```python
if condition_1:
    if condition_2:
        print("1 and 2")
    elif condition_3:
        print("1 and 3")
    else:
        print("1 and not 2 or 3")
elif condition_4:
    if condition_2:
        print("4 and 2")
    elif condition_3:
        print("4 and 3")
    else:
        print("4 and not 2 or 3")
else:
    print("neither 1 nor 4")
```

## Variable Scope

**Variable scope** refers to what parts of the code a particular variable is accessible in. Python uses **function scope**, which means that a variable defined anywhere in a function is available below that definition in any part of the same function.

Other languages use **block scope**, where variables are only available within the block where they are defined. 

