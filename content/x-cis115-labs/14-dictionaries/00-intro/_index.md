---
title: "Introduction"
pre: "0. "
weight: 01
date: 2021-04-23T00:00:01-05:00
---

{{< youtube RnwIej2eA-o >}}

Previously, we learned how we can use lists in Python to store multiple values, or elements, in a single variable. Each element in a list is given an index, which allows us to uniquely reference and identify each element's position in a list. Python lists use consecutive integers starting at $0$ as indexes, which makes for a pretty easy to use data structure.

However, what if we would like to use some other value besides an integer as the index? For example, if we create a data structure to store information about a user account, wouldn't it be much easier if we could use the username as the index, allowing us to quickly find that particular user's data? 

Thankfully, Python includes another built-in data structure, called a **dictionary**, that allows us to do exactly that. In a dictionary, instead of indexes we have **keys**, which can be _any_ data type, that uniquely identify each item, or **value**, in the dictionary. Other programming languages refer to dictionaries as **hash tables**, **hash maps**, or **associative arrays**, which gives a clue to how they work behind the scenes.

In this lab, we'll learn how to create and use dictionaries in Python. Dictionaries are a very powerful and useful data structure in Python, with many uses. Let's see how they work!