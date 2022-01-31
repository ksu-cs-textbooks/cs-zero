---
title: "Python Strings"
pre: "6. "
weight: 60
date: 2021-01-29T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="slides" target="_blank">Slides</a>

Python also includes an operator that can be used to concatenate two strings together. Just like in pseudocode, we can use the plus symbol `+` between two strings to concatenate them together into a single string, making it much simpler to build more complex strings and outputs. 

A simple example is shown below:

```python
first = "Hello"
second = "World"
print(first + second)
```

When executed, this code will display this output:

```tex
Hello World
```

As we can see, using the `+` operator in Python to concatenate two strings together is a quick and easy way to simplify our print statements.

## Concatenating Numbers

Just like in pseudocode, Python also requires both sides of the `+` operator to be strings in order for concatenation to work. So, if we want to concatenate a string with a numeric value, we'll have to convert it to a string using the special `str()` function. Here's an example:

```python
text = "Your total is $"
value = 2.75
print(text + str(value))
```

When we run this program, we'll receive the following output:

```tex
Your total is $2.75
```

However, if we forget to convert the `value` variable to a string, as in this example:

```python
text = "Your total is $"
value = 2.75
print(text + value)
```

we'll receive an error instead:

```tex
Traceback (most recent call last):
  File "tutor.py", line 3, in <module>
    print(text + value)
TypeError: must be str, not float
```

So, we'll have to be careful and make sure that we convert all of our numbers to strings before trying to concatenate them together. Of course, if both sides of the `+` operator are numbers, then it will perform addition instead of concatenation!

## String Formatting

Python also includes another method of building strings, and that is the `format()` method. The `format()` method allows us to put placeholders in strings that are later replaced with values from variables, effectively creating a way to build "templates" that can be used throughout our program.

The easiest way to see how this works is looking at a few examples. Let's start with a simple one:

```python
name = input("Enter your name: ")
print("Hello {}".format(name))
```

If the user inputs `"Willie Wildcat"` when prompted, then this code will produce this output:

```tex
Enter your name: Willie Wildcat
Hello Willie Wildcat
```

There are many important parts to this example, so let's look at each one individually. First, in the `print()` statement, we see the string `"Hello {}"`. This is an example of a **template string**, which includes a set of curly braces `{}` as **placeholders** for data to be inserted. Each template string can have unlimited sets of curly braces, and each one will be given a different piece of data from the `format()` method.

Then, we see a period `.`, followed by the `format()` method. Notice that the format method is directly attached to the template string by a period - this is because it is actually a method that operates on the template string object itself. This is a key concept in object-oriented programming, which we won't cover in detail right now, but we'll definitely see it come up later as we learn more about programming. This is also why we are referring to `format()` as a **method** instead of a **function**, since it is directly attached to another object.

When executed, the format method will replace the placeholders in the string with the values provided as arguments, working from left to right. The first argument will replace the first placeholder, and so on, until all placeholders are replaced and the arguments are all used.

The `format()` method itself can have unlimited arguments. Each argument corresponds with one of the placeholders in the template string. So, if there are two placeholders, there should also be two arguments. 

{{% notice note note-1 "Advanced Formatting" %}}

The Python `format()` method can do many powerful things, such as place the same argument in multiple placeholders, and each placeholder can define how a value should be presented to the user, among many other features. For right now, we'll just use simple, empty placeholders in our template strings. Likewise, we'll just deal with the situation where each placeholder matches to exactly one argument to the `format()` method. 

{{% /notice %}}

The most powerful use of the string `format()` method is to insert numerical values directly into strings without having to convert each value directly to the `str` data type - the `format()` method handles that conversion for us.

For example, we can update our previous program to use the string `format()` method to display the output in a single `print()` statement, and we can also add additional information with ease:

```python
text_one = input("Enter the price of one item: ")
price = float(text_one)
text_two = input("Enter the quantity of items: ")
quantity = int(text_two)
cost = price * quantity
print("{} items at ${} each is ${} total".format(quantity, price, cost))
```

When we execute this program, we'll see output that looks like this:

```tex
Enter the price of one item: 2.75
Enter the quantity of items: 3
3 items at $2.75 each is $8.25 total
```

This example shows how easy it is to build complex output strings using a simple template string and the string `.format()` method. 

