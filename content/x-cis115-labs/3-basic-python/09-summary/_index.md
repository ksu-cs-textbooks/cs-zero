---
title: "Summary"
pre: "9. "
weight: 90
date: 2021-01-15T00:00:01-05:00
---

In this lab, we introduced some basic statements and structures in the Python programming language. Let's quickly review them!

## Print Statement

The `print(expression)` statement is used to print output on the terminal.

1. It will evaluate `expression` to a value, then display it to the screen.
1. By default, it will add a newline to the end of the output.
1. We can change that using the `end` parameter, such as `print(expression, end="")` to remove the newline.

## Assignment Statement

The assignment statement, like `a = expression` is used to create variables and store values in the variables.

1. The variable must be on the left side, and the right side must be an expression that evaluates to a single value.
1. If the variable does not exist, it is created. Otherwise, the current value of the variable is replaced by the new value.
1. Variable names must begin with a letter or underscore, and may only contain letters, numbers, and underscores.
1. Variable names beginning with an underscore have a special meaning, so we won't use them right now.


## Functions

A function is a piece of code that is given a name, which can then be run by calling it elsewhere in the program.

To create a function, we use the following structure:

```python
def function_name(parameter1, parameter2):
    <block of statements>
```

1. Function names follow the same rules as variable names.
1. Functions may require 0 or more parameters, placed in parentheses after the function name. Multiple parameters are separated by commas.
1. When called, a function will run the lines of code indented beneath the function definition.

To call a function, we use the following structure:

```tex
function_name(argument1, argument2)
```

1. A function call is the function name, followed by parentheses `()`.
1. Inside of the parentheses, a matching argument must be included for each parameter required by the function. Multiple arguments are separated by commas.
1. Each argument may be an expression that evaluates to a value.
1. The values of each argument are copied into the function. When the function ends, the original arguments are unchanged. 

## Summary

As we've seen, the Python language is very similar to the pseudocode language we've already learned about. Hopefully the practice we have in reading and writing pseudocode using our "mental model" of a computer will help make it even easier to read and write Python code that is meant to be run on an actual computer. 
