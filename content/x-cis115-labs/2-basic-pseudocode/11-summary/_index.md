---
title: "Summary"
pre: "11. "
weight: 110
date: 2021-01-07T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="slides" target="_blank">Slides</a>

In this lab, we introduced a simple pseudocode programming language, based on the one used by the [AP Computer Science Principles](https://apcentral.collegeboard.org/pdf/ap-computer-science-principles-exam-reference-sheet.pdf) exam. This pseudocode language includes several statements and rules we've learned to use in this lab. Let's quickly review them!

## Display Statement

The `DISPLAY(expression)` statement is used to display output to the user.

1. It will evaluate `expression` to a value, then display it to the screen.
1. It does not add any additional spaces or newlines after the value is displayed
1. We can display spaces using `DISPLAY(" ")`, and we can use the newline symbol to go to the next line `DISPLAY("\n")`

## Assignment Statement

The assignment statement, like `a <- expression` is used to create variables and store values in the variables.

1. The variable must be on the left side, and the right side must be an expression that evaluates to a single value.
1. If the variable does not exist, it is created. Otherwise, the current value of the variable is replaced by the new value.
1. Variable names must begin with a letter, and may only contain letters, numbers, and underscores. 

## Procedures

A procedure is a piece of code that is given a name, which can then be run by calling it elsewhere in the program.

To create a procedure, we use the following structure:

```tex
PROCEDURE procedure_name(parameter1, parameter2)
{
    <block of statements>
}
```

1. Procedure names follow the same rules as variable names.
1. Procedures may require 0 or more parameters, placed in parentheses after the procedure name. Multiple parameters are separated by commas.
1. When called, a procedure will run the lines of code placed between the curly braces `{}`. These lines of code are indented to make it clear that they are part of the procedure.

To call a procedure, we use the following structure:

```tex
procedure_name(argument1, argument2)
```

1. A procedure call is the procedure name, followed by parentheses `()`.
1. Inside of the parentheses, a matching argument must be included for each parameter required by the procedure. Multiple arguments are separated by commas.
1. Each argument may be an expression that evaluates to a value.
1. The values of each argument are copied into the procedure. When the procedure ends, the original arguments are unchanged. 

## Summary

This pseudocode language may seem very simple, but we've already learned a great deal about how programming works and how a computer interprets a program's code, just by practicing with this very simple language. In the next lab, we'll see how these concepts directly relate to a real programming language, Python. For now, feel free to keep practicing by writing programs and pseudocode and running them on your "mental model" of a computer. It is a very important skill to develop!