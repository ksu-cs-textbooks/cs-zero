---
title: "Pseudocode Variables"
pre: "4. "
weight: 40
date: 2021-01-07T00:00:01-05:00
---

{{< youtube 7lau4NnO4hg >}}

#### Resources

* <a href="slides" target="_blank">Slides</a>

Now that we've learned how to use the `DISPLAY(expression)` statement, let's focus on the next major concept in pseudocode, as well as any other programming language: **variables**. 

The word **variable** is traditionally defined as a value that can change. We've seen variables like $x$ used in Algebraic equations like $x + 4 = 7$ to represent unknown values that we can try to work out. In programming a **variable** is defined as a way to store a value in a computer's memory so we can retrieve it later. One common way to think of variables is like a box in the real world. We can put something in the box, representing our value. Likewise, we can write a name on the side of the box, corresponding to our variable's name. When we want to use the variable, we can get the value that it currently stores, and even change it to a different value. It's a pretty handy mental metaphor to keep in mind!

## Creating Variables

To use a variable, we must first create one. In pseudocode, we create a variable in a special type of statement called an **assignment statement**. The basic structure for an assignment statement is `a <- expression`. When our "mental model" runs this statement, it will first evaluate `expression` into a single value. Then, it will store that same value (we can think of this as a _copy_ of that value) in the variable named `a`. For example, the statement:

```tex
x <- "Hello World"
```

will store the string value "Hello World" into a new variable named `x`. Pretty handy! 

Now, let's cover some important rules related to assignment statements:

1. Assignment statements are always written with the variable on the left, and an expression on the right. We cannot reverse the statement and say `expression -> x` in programming like we can in math. In mathematical terms, this means an assignment statement is not commutative. 
1. The left side of an assignment statement must be a location where a value can be stored. For now, we only have single variables in our pseudocode so that's all we'll use, but later on in this course we'll learn about lists as another way to store data. 
1. The right side of an assignment statement must be an expression that evaluates to a value that can be stored in the location given on the left side. We'll spend more time discussing this in future labs, but it is an important rule to know. 

## Using Variables

Once we've created a variable, we can use a variable in an **expression** to retrieve its current value. For example, we can now rewrite our previous "Hello World" program to use a variable like this:

```tex
x <- "Hello World"
DISPLAY(x)
```

Notice that we **don't** put quotes around the variable `x` in the `DISPLAY(expression)` statement like we did before. This is because we want to evaluate the variable `x` and display the value it contains, not display the string `"x"`. Remember that quotes are only placed around string values, but variables are used without quotes around them. So, when we run this program on our "mental model" of a computer, we should get this output:

```tex
Hello World
```

Great! We've learned how to use variables in our programs.

## Updating Variable Values

We can easily update the value stored in a variable by simply using another **assignment statement** in our code. For example, consider this program that displays two lines of output:

```tex
x <- "First line\n"
DISPLAY(x)
x <- "Second line"
DISPLAY(x)
```

When we run this program, we should see the following output:

```tex
First line
Second line
```

Notice how we are printing the variable `x` twice in the program, but each time it displayed a different value? This is because the value stored in `x` can change while the program is running, but when we evaluate it, we only get the value that it is currently storing. This is why we call items like `x` variables - because their value can change!

{{% notice note note-2 "Variable Names" %}}

Let's talk about variable names for a minute. There is an old joke in computer science that says "the two most difficult things in computer science are dealing with cache invalidation and naming things." We won't learn about cache invalidation for a while (it's a pretty advanced topic), but as we spend more time writing code, we'll probably find out that coming up with good and useful variable names can indeed be difficult. It might even derail your progress for a bit while you try to come up with the most perfect variable name ever.

Most languages have some rules for how variables should be named, and our pseudocode is no different. Likewise, there are some conventions that most programmers follow when naming variables, even though they aren't required to. Thankfully, these conventions can be bent or broken at times depending on the situation.

In this course, we'll follow the following **rules** when it comes to naming variables:

1. A variable name must begin with a letter.
1. Variable names must only include letters, numbers, and underscores. No other symbols, including spaces, are allowed.

Beyond that, here are a few **conventions** that you should follow when naming your variables:

1. Variables should have a descriptive name, like `total` or `average`, that makes it clear what the variable is used for.
1. Variables should be named using [Snake Case](https://en.wikipedia.org/wiki/Snake_case). This means that spaces are represented by underscores `_`, as in `number_of_inputs`
1. Try to use traditional variable names only for their specific uses. Some examples of traditional variable names:
    1. `tmp` or `temp` are temporary variables.
    1. `i`, `j`, and `k` are iterator variables (we'll learn about those later).
    1. `x`, `y`, and `z` are coordinates in a coordinate plane.
    1. `r`, `g`, `b`, `a` are colors in an RGB color system.
1. Variables should not have the same name as keywords or any built-in statements or expressions in the language.
    1. For example, our pseudocode has a `DISPLAY()` statement, so we should not name a variable `DISPLAY` in our language.
1. In general, longer variable names are more useful than short ones, even if they are more difficult to type.

That said, in many of the code reading and writing examples in this course, you'll see lots of simple variable names that **are not** descriptive at all. This is because the point of the exercise is to read and understand the code itself, not simply inferring what it does based on the variable names. We'll still follow the **rules**, but we may ignore some or all of the **conventions** in our code. 

{{% /notice %}}