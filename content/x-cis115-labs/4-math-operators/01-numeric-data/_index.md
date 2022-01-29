---
title: "Numeric Data"
pre: "1. "
weight: 10
date: 2021-01-29T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="slides" target="_blank">Slides</a>

Previously, we learned about **strings** and **string values** in pseudocode. Recall that a string is just text inside of a set of quotation marks `""`, such as `"Hello World"` or `"Willie Wildcat"`. In technical terms, a string is an example of a **data type** in programming. A **data type** defines the way a particular value can be stored in a computer. For text values, we use the string data type.

What about numbers? We all know how important numbers can be, especially since we've probably spent more time studying mathematics than just about any other subject in school. So, let's introduce a new data type in pseudocode called the **number** data type. This data type can store any single number, such as $1$ or $2.3$ or even special numbers like $\pi$ (pi) or $e$ (Euler's number). 

So, to create an expression that evaluates to a numerical value in pseudocode, we can just use the numbers in our code instead of text in quotes. For example, to store then number $7$ in a variable, we'd use the following **assignment statement** in pseudocode:

```tex
num1 <- 7
```

Notice that the numerical value `7` in our code does not have quotation marks around it. This is because we want to treat it like a numerical value instead of a string.

Also, recall from earlier that we cannot use a number as the first symbol in a variable name? This is because numerical values must always start with a number, so we enforce this rule to allow us to tell the difference between numerical values and variable names.


For a number with a decimal in it, such as $1.23$, we can use a similar process:

```tex
num2 <- 1.23
```

If we have a value that is less than $1$, we must put a `0` in front of the decimal point, like this:

```tex
num3 <- 0.42
```

We can also create negative values by placing the negative symbol `-` (the same symbol as the minus sign) in front of the numerical value:

```tex
num4 <- -4.56
```

Notice that we have to be careful to include a space between the arrow symbol `<-` in the assignment statement and the negative symbol `-` for a negative value. 

As we can see, creating variables that store numerical values is pretty easy, and it hopefully works exactly like you expect it to work.

## Converting Between Data Types

Now that we have two different data types, **strings** and **numbers**, it might be useful to convert between the two data types. Officially, the [AP Pseudocode](https://apcentral.collegeboard.org/pdf/ap-computer-science-principles-exam-reference-sheet.pdf) does not include an explicit way to convert between data types, or any concept of different data types at all. Instead, they just assume that variables can "automagically" convert data as the developer intended, without performing any additional steps.

However, this can get a bit confusing, so we'll briefly introduce two different procedures in pseudocode that can handle converting data between different types.

To convert any type of data to a **number**, we can use the `NUMBER(expression)` procedure. It will evaluate the `expression` to a value, and then convert that value to a number. Of course, this requires us to make sure that whatever value we get when we evaluate the `expression` will make sense as a number. Since we aren't running this on a real computer, we don't have to worry about any errors or crashes - instead, it will just mean that our program won't make any sense when we try to run it on our "mental model" of a computer. 

Likewise, to convert any data to a **string**, we can use the `STRING(expression)` procedure in a similar way. Thankfully, pretty much any value in any data type can be represented as a string in some way, so we don't have to worry about this procedure causing issues if the `expression` results in a strange value. 