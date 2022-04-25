---
title: "Loops with Dictionaries"
pre: "2. "
weight: 20
date: 2021-04-23T00:00:01-05:00
---

{{< youtube SgqDwc--C-Q >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Another useful way we can work with dictionaries in Python is by iterating through them. In Python 3.6 and beyond, the items in a dictionary will be presented in the same order that they were added to the dictionary. This isn't always the case in other languages or older versions of Python

## Loops with Dictionaries - Keys

There are two ways we can iterate through a dictionary in Python. Below is an example of the first, and simplest, method:

```python
dict_3 = {
    "cat": "mammal",
    "lizard": "reptile",
    "goldfish": "fish",
    "chickadee": "bird"
}

for key in dict_3:
    print("{}: {}".format(key, dict_3[key]))
```

In this method, we are iterating through the entire dictionary using a for loop. However, the dictionary will only store the **key** for each key-value pair in the iterator variable. So, to access the value associated with the key, we can simply place it in square brackets after the dictionary's variable name. 

When we run this program, we should see the following output:

![Output 1](/images/lab14/output1.png)

As we can see, it will print each key-value pair in the dictionary, one per line.

## Loops with Dictionaries - Keys and Values

The other method we can use when looping through a dictionary allows us to access both the keys and values directly within the loop. Here's an example of using that method:

```python
dict_3 = {
    "cat": "mammal",
    "lizard": "reptile",
    "goldfish": "fish",
    "chickadee": "bird"
}

for key, value in dict_3.items():
    print("{}: {}".format(key, value))
```

In this method, instead of iterating through the dictionary itself, we iterate through the `items()` in the dictionary. When we call the `items()` function in a dictionary, we are given a list of the key-value pairs that it contains, and each key-value pair is stored as a **tuple**. From there, we can access each of the elements in the tuple individually using a comma `,` between two variable names. It is a bit complex, and touches on a few concepts in Python that we won't cover in this course, but hopefully it makes sense by looking at the code.

When we run this program, we'll receive the same output as the previous example:

![Output 1](/images/lab14/output1.png)

While iterating through dictionaries is not as common as iterating through lists, it is still very important to know that it can be done. Hopefully you'll find this example useful as you continue to work with dictionaries in Python.