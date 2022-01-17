---
title: "Summary"
pre: "9. "
weight: 90
date: 2021-01-15T00:00:01-05:00
---

## Pseudocode Procedures

A procedure in pseudocode is a piece of code that is given a name, which can then be run by calling it elsewhere in the program.

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

## Python Functions

A function in Python is a piece of code that is given a name, which can then be run by calling it elsewhere in the program.

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

As we've seen, procedures in pseudocode and functions in Python are very similar. They allow us to write pieces of code that we can use repeatedly throughout our programs. This makes our programs more organized and modular, and will make it much easier to write more complex programs as we continue to develop our skills.s
