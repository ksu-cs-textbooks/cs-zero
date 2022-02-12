---
title: "Variables"
pre: "5. "
weight: 50
date: 2021-01-15T00:00:01-05:00
---

{{< youtube _iuCFOGvtP0 >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

The `print(expression)` statement is very powerful in Python, but we really can't do much with our programs using just a single statement. So, let's look at how we can use **variables** in Python as well.

Recall that a **variable** is a value that can change. In programming, it is easiest to think of a variable as a place in memory where we can store a value, and then we can recall it later by using that variable in an expression. In a later lab, we'll learn how to use operators to manipulate the values stored in variables, but for right now we're just going to focus on storing and retrieving data using variables.

## Creating Variables

The process for creating a variable in Python is very similar to what we observed in pseudocode. Once again, we're going to use an **assignment statement** to create a variable by storing a value in that variable. An assignment statement in Python looks like `a = expression`, where `a` is the name of a variable, and `expression` is an expression that evaluates to a value that we can store in that variable. For example, let's consider the Python statement:

```python
x = "Hello World"
```

In that statement, we are storing the string value `"Hello World"` in the variable named `x`. It's just like we expect it to work based on what we've already learned in pseudocode. 

Let's review some of the important rules about variables that we've learned so far:

1. Assignment statements are always written with the variable on the left, and an expression on the right. This is a bit more confusing in Python, since we are used to the equals `=` symbol being commutative in math, meaning that we can swap the left and right side and it will still be a true statement. However, in Python, the equals `=` symbol is only used for assignment statements, and it must always have the variable on the left and an expression on the right. 
1. The left side of an assignment statement must be a location where a value can be stored. Once again, we're just going to work with single variables, so we don't have to worry about this yet. In a later lab, we'll introduce lists as another way to store data, and we'll revisit this rule.
1. The right side of an assignment statement must be an expression that evaluates to a value that can be stored in the location given on the left side. Similar to the rule above, right now we're only working with string values, so we don't have to worry about this rule yet. We'll come back to it in a future lab.

## Using Variables

Once we've created a variable, we can use it in any **expression** to recall the current value stored in the variable. So, we can extend our previous example to store a value in a variable, and then use the `print(expression)` statement to display it's value. Here's what that would look like in Python:

```python
x = "Hello World"
print(x)
```

Just like in pseudocode, notice that we don't put quotation marks `"` around the variable `x` in the `print(expression)` statement. This is because we want to display the value stored in the variable `x`, not the string value `"x"`. So, when we run this code, we should get this output:

```tex
Hello World
```

To confirm, feel free to try it yourself! Copy the code above into a Python file, then use the `python3` command in the terminal to run the file and see what it does. Running these examples is a great way to learn how a computer actually executes code, and it helps to confirm that your "mental model" of a computer matches how a real computer operates. 

## Updating Variable Values

Python also allows us to change the value stored in a variable using another **assignment statement**. For example, we can write some Python code that uses the same variable to print multiple outputs:

```python
a = "Output 1"
print(a)
a = "Output 2"
print(a)
```

When we run this code, we'll see the following output:

```tex
Output 1
Ouptut 2
```

So, just like we observed in pseudocode, when we evaluate a variable in code, it will result in the value currently stored in that variable at the time it is evaluated. So, even though we are printing the same variable twice, each time it is storing a different value. Recall that this is why we call items like `a` a **variable** - their value can change!

## Variable Names

Finally, Python uses many of the same rules for variable names that we introduced in pseudocode. Let's quickly review those rules, as well as some conventions that most Python developers follow when naming variables.

First, the **rules** that must be followed:

1. Variable names must begin with either a letter or an underscore `_`.
1. Variable names may only contain letters, numbers, and underscores `-`.
1. Variable names are case sensitive. 

Next, here are the **conventions** that Python developers follow for variable names, which we will also follow in this course:

1. Variable names beginning with an underscore `_` have a special meaning. So, we won't create any variables beginning with an underscore right now, but later we'll learn about what they mean and start using them.
1. Variables should have a descriptive name, like total or average, that makes it clear what the variable is used for.
1. Variables should be named using [Snake Case](https://en.wikipedia.org/wiki/Snake_case). This means that spaces are represented by underscores `_`, as in `number_of_inputs`
1. Try to use traditional variable names only for their specific uses. Some examples of traditional variable names:
    1. `tmp` or `temp` are temporary variables.
    1. `i`, `j`, and `k` are iterator variables (we'll learn about those later).
    1. `x`, `y`, and `z` are coordinates in a coordinate plane.
    1. `r`, `g`, `b`, `a` are colors in an RGB color system.
1. Variables should not have the same name as keywords or any built-in statements or expressions in the language.
    1. For example, Python has a `print` statement, so we should not name a variable `print` in our language.
1. In general, longer variable names are more useful than short ones, even if they are more difficult to type.

Finally, don't forget that some of the code examples in this course will not follow these conventions, mainly because long, descriptive variable names might give away the purpose of the code itself. We'll still follow the **rules** that are required, but in many cases we'll use simple variable names so that the focus is learning to read the structure of the code, not inferring what it does based solely on the names of the variables. 