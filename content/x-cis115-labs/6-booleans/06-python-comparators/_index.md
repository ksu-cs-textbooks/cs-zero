---
title: "Python Comparators"
pre: "6. "
weight: 60
date: 2021-02-11T00:00:01-05:00
---

{{< youtube QE5Lb58y1wI >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Python also uses various **comparators** to allow us to compare values of many different data types to produce a Boolean value. We can compare numbers, strings, and many other data types in Python using these comparators.

Since we've already covered the comparators in pseudocode, let's just briefly go over all of them and discuss any ways they differ in Python compared to pseudocode.

The basic comparators in Python are:

* `==` equal
* `!=` not equal
* `<` less than
* `<=` less than or equal to
* `>` greater than
* `>=` greater than or equal to

Notice that the equal comparator in Python now uses two equals signs `==` instead of a single one. This is because the single equals sign `=` is used in the assignment statement, and we don't want to confuse a Boolean comparator for an assignment. So, in Python, as in most other programming languages, we use two equals signs `==` when comparing values, and one equals sign `=` when we are storing a value in a variable.

## Comparing values

Just like in pseudocode, we usually only want to compare values of the same data type using comparators. It really only makes sense to compare strings to strings, and booleans to booleans. However, for the numeric data types `int` and `float`, we can easily compare values of either data type together in Python.

Consider the following example:

```python
x = 5
y = 5.0
print(x == y)
```

When we execute this code, we'll get this output:

```tex
True
```

Even though `x` is the `int` data type and `y` is the `float` data type, they both store the same numerical value, and our comparators will work just like we expect. So, we can easily compare both integers and floating-point values in our code.

{{% notice note note-1 "Coercion" %}}

Behind the scenes, when we compare an `int` and a `float` value in Python, Python will convert the values to a common data type, usually the `float` data type, using the appropriate conversion function. This is known as **coercion** in programming - the program is essentially forcing a value of one data type into another data type because of an operation. However, it won't change the data type of the variable involved, just the value it is evaluating. 

{{% /notice %}}

Strings in Python can also be compared using the various comparator operators. When two strings are compared using any type of "less than" or "greater than" comparator, they will be compared according to their [lexicographic order](https://en.wikipedia.org/wiki/Lexicographic_order). In general, this means that each letter will be ordered based on its value in the [ASCII](https://en.wikipedia.org/wiki/ASCII) encoding standard.

Let's look at a quick example:

```python
a = "First"
b = "fir"
print(a < b)
```

When we run this code, we'll see this output:

```tex
True
```

This may seem surprising, since we'd expect the word `"fir"` to come before the word `"First"` in a dictionary, since it has fewer letters. However, in Python, the letters `"f"` and `"F"` are not treated identically. According to the [ASCII](https://en.wikipedia.org/wiki/ASCII) encoding standard, capital letters have a lower value than lower-case letters, so all words starting with a capital `"F"` will come before any words starting with a lower-case `"f"`. 

This can be a bit confusing, so it is always important to remember that we can always write a quick sample program in Python to test how a particular operator will work for a given set of values. If nothing else, we can always count on our computer to produce the same result for the same operation, no matter if it is part of a larger program or a small test program.

## Order of Operations

Finally, Python's order of operations follow the same rules that we saw in pseudocode. So, when we see an expression that combines mathematical operators with Boolean operators and comparators, we'll follow this order:

1. Math operators (according to their order of operations)
1. Boolean comparators
1. `not` operator
1. `and` operator
1. `or` operator

As always, it is considered good practice to include parentheses in any complex expressions to make sure that the intent is clear, regardless of the order of operations. 