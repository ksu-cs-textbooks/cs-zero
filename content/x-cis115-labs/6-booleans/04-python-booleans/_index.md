---
title: "Python Booleans"
pre: "4. "
weight: 40
date: 2021-02-11T00:00:01-05:00
---

{{< youtube GNV4bRAAQlk >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

In Python, Boolean values are stored in the `bool` data type. Just like in pseudocode, variables of the `bool` data type can only store one of two values, `True` or `False`. 

To create a Boolean variable in Python, we can simply assign those values to a variable in an assignment statement:

```python
a = True
b = False
print(a)
print(type(b))
```

When we execute that code, we'll see the following output:

```tex
True
<class 'bool'>
```

In Python, we use the **keywords** `True` and `False` to represent Boolean values. Notice that they are capitalized, unlike the `true` and `false` values we saw in pseudocode. In Python, it is very important to make sure these values are capitalized, otherwise the program will not work properly. Also, since these are keywords and not strings, we don't need to put them in quotation marks.

## Converting Between Data Types

Python includes the special `bool()` function, which can be used to convert any data type into a Boolean value. The `bool()` function follows these rules to determine what to return:

1. If the input is the value `False`, the value `0`, the value `None`, or anything with 0 length, including the empty string, it will return `False`.
1. Otherwise, for all other values it will return `True`.

Let's look at a couple of quick examples. First, let's try to convert the strings `"True"` and `"False"` to their Boolean equivalents:

```python
print(bool("True"))
print(bool("False"))
```

When this code is executed, we'll see this output:

```tex
True
True
```

This seems a bit strange, since the string `"False"` ended up creating the Boolean value `True`. However, if we look at the rules above, since the string `"False"` has a length greater than 1, and it is not any of the special values listed above, it should always result in the Boolean value `True`. 

In this example, we can check a couple of special values using the `bool()` function:

```python
print(bool(0))
print(bool(1))
print(bool(""))
```

In this case, we'll see the following output:

```tex
False
True
False
```

Here, we see that the value `0`, as well as the empty string `""`, both result in a value of `False`. However, the value 1 is `True`, since it is a non-zero value.

In practice, we won't use the `bool()` function directly very often. Instead, if we want to determine if a user inputs a `True` or `False` value, we can just use one of the Boolean comparators that we'll see later in this lab. 
