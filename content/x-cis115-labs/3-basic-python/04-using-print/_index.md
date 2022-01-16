---
title: "Using Print"
pre: "4. "
weight: 40
date: 2021-01-15T00:00:01-05:00
---

{{< youtube BhpTb-i4ELg >}}

#### Resources

* <a href="slides" target="_blank">Slides</a>

The `print(expression)` statement in Python works in much the same way as the `DISPLAY(expression)` statement in pseudocode, but with one major difference. In pseudocode, the `DISPLAY(expression)` statement will print the value from the expression to the user, but it won't add anything like a space or newline to the end. In Python, however, the `print(expression)` statement will add a newline to the end of the output by default. This means that multiple `print(expression)` statements will print on multiple lines. Let's look at some examples!

Throughout this course, we'll show many different code examples and their output here in the lab. To test them out, feel free to copy the code examples to a Python file and run it yourself. You can even tweak them to do something new and see how Python interprets different pieces of code. In the end, the best way to learn programming is to explore, and running these examples on your own is a great way to get started!

## Multiple Lines

In Python, we can print multiple lines of output simply by using multiple `print(expression`) statements:

```python
print("a")
print("b")
print("c")
print("d")
```

will result in this output:

```tex
a
b
c
d
```

We can also include a newline symbol `\n` in a `print(expression)` statement in Python. This will add a newline to the output, and then the `print(expression)` statement will add an additional newline at the end of the value that is printed:

```python
print("one\ntwo")
print("three\nfour")
```

will produce this output:

```tex
one
two
three
four
```

## Printing On the Same Line

What if we want to display multiple `print(expression)` statements on the same line? To do that, we must add an additional option to the `print(expression)` statement - the `end` option. 

For example, the following code will produce output all on the same line:

```python
print("Hello ", end="")
print("World!")
```

In this example, we set `end` to be an empty string `""`. When we run this program, we'll get the following output:

```tex
Hello World!
```

In fact, in Python, the `print(expression)` statement is an example of a **function** in Python. **Functions** in Python are like procedures in pseudocode - when we call them, we write the name of the function, followed by a set of parentheses and then arguments separated by commas within the parentheses. So, in actuality, the `expression` in the `print(expression)` statement is just the first argument when we call the `print` function. 

Therefore, the `end` option that we showed above is just a second argument that is optional - it simply let's us choose what to put at the end of the output. By default, the `end` parameter is set to the newline symbol `\n`, so if we don't provide an argument for `end` it will just add a newline at the end of the value.

We can set the value of `end` to be any string. If we want to include a space at the end of the output, we can add `end=" "` to the `print` function call. 

In this course, we won't spend much time talking about optional parameters and default values in Python functions, but it is important to understand that statements like `print` are actually just Python functions behind the scenes!