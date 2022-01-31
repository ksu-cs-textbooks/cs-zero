---
title: "String Concatenation"
pre: "2. "
weight: 20
date: 2021-01-29T00:00:01-05:00
---

{{< youtube lY0CBvYNgyw >}}

#### Resources

* <a href="slides" target="_blank">Slides</a>

So far we've only looked at operators that can be used on two numeric values, but there are also a few operations we can perform on strings as well. Let's look at one important operator that is commonly used with strings - the concatenation operator. In pseudocode, like most other programming languages, we'll use the plus symbol `+` to represent the concatenation operator. 

The term **concatenate** may be a new term, since it isn't used very often outside of programming. To **concatenate** two items, we are simply linking two items together, one after the other. When applied to strings, we can use the concatenate operator to combine two strings into a single string.

Let's look at an example:

```tex
one <- "Hello"
two <- "World"
message <- one + " " + two
DISPLAY(message)
```

In this code, we begin with the strings `"Hello"` and `"World"` stored in two separate variables, `one` and `two`. Then, we create a new variable `message`, which contains the values of `one` and `two` concatenated together, with a space in between. Since `one` and `two` are strings instead of numbers, we know the `+` symbol represents the concatenate operation, instead of addition.

When we run this program on our "mental model" of a computer, we should see this output:

```tex
Hello World
```

As we can see, the concatenate operator is a way we can build complex strings from various parts.

## Concatenating Numbers

Because the concatenate operator works with strings, we have to add a couple of rules to how our pseudocode language handles data types to deal with this. Here are the most important rules to follow:

1. If both sides of the `+` operator are strings, then the `+` operator is treated like a concatenation. If both sides are numbers, then it is treated like addition. The `+` operator cannot be applied to a string and a number.
1. The concatenation operation always returns a string.

This may seem a bit confusing to anyone who has experience with programming, since many programming languages allow us to use the `+` operator between strings and numbers without any issues. However, in this case we're going to stick closely with what is allowed in Python, so these are the rules we'll follow in pseudocode.