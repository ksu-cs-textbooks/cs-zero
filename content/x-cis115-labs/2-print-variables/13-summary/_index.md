---
title: "Summary"
pre: "13. "
weight: 130
date: 2021-01-07T00:00:01-05:00
---

## Pseudocode

In this lab, we introduced a simple pseudocode programming language, based on the one used by the [AP Computer Science Principles](https://apcentral.collegeboard.org/pdf/ap-computer-science-principles-exam-reference-sheet.pdf) exam. This pseudocode language includes several statements and rules we've learned to use in this lab. Let's quickly review them!

### Display Statement

The `DISPLAY(expression)` statement is used to display output to the user.

1. It will evaluate `expression` to a value, then display it to the screen.
1. It does not add any additional spaces or newlines after the value is displayed
1. We can display spaces using `DISPLAY(" ")`, and we can use the newline symbol to go to the next line `DISPLAY("\n")`

### Assignment Statement

The assignment statement, like `a <- expression` is used to create variables and store values in the variables.

1. The variable must be on the left side, and the right side must be an expression that evaluates to a single value.
1. If the variable does not exist, it is created. Otherwise, the current value of the variable is replaced by the new value.
1. Variable names must begin with a letter, and may only contain letters, numbers, and underscores. 

### Summary

This pseudocode language may seem very simple, but we've already learned a great deal about how programming works and how a computer interprets a program's code, just by practicing with this very simple language. In the next lab, we'll see how these concepts directly relate to a real programming language, Python. For now, feel free to keep practicing by writing programs and pseudocode and running them on your "mental model" of a computer. It is a very important skill to develop!

<hr>

## Python

We also introduced some basic statements and structures in the Python programming language. Let's quickly review them!

### Print Statement

The `print(expression)` statement is used to print output on the terminal.

1. It will evaluate `expression` to a value, then display it to the screen.
1. By default, it will add a newline to the end of the output.
1. We can change that using the `end` parameter, such as `print(expression, end="")` to remove the newline.

### Assignment Statement

The assignment statement, like `a = expression` is used to create variables and store values in the variables.

1. The variable must be on the left side, and the right side must be an expression that evaluates to a single value.
1. If the variable does not exist, it is created. Otherwise, the current value of the variable is replaced by the new value.
1. Variable names must begin with a letter or underscore, and may only contain letters, numbers, and underscores.
1. Variable names beginning with an underscore have a special meaning, so we won't use them right now.

### Summary

As we've seen, the Python language is very similar to the pseudocode language we've already learned about. Hopefully the practice we have in reading and writing pseudocode using our "mental model" of a computer will help make it even easier to read and write Python code that is meant to be run on an actual computer. 

