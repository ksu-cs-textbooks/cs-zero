---
title: "Display Statement"
pre: "2. "
weight: 20
date: 2021-01-07T00:00:01-05:00
---

{{< youtube MKbEdl0yjJU >}}

#### Resources

* <a href="slides" target="_blank">Slides</a>

First, let's start by introducing some important vocabulary terms:

* **string**: A **string** in programming is any text that is stored as a value. We typically represent strings by placing them inside double quotes `""` in our code and elsewhere.
* **value**: A **value** is a piece of data that our program is storing and manipulating. In our pseudocode, values consist of either numbers or strings.
* **keyword**: A **keyword** is a reserved word in a programming language that defines a particular statement, expression, structure, or other use. As we'll learn later, we cannot use these keywords as variable or procedure names.
* **statement**: A **statement** refers to a piece of code that performs an action, but doesn't result in any value. Most complete lines of code are considered statements.
* **expression**: An **expression**, on the other hand, is a piece of code that, when evaluated, will result in a value that can be used or stored. An expression can even contain multiple expressions inside of it!

Now that we have learned a few of the important terms used in programming, we can start to discuss the various statements in pseudocode. 

In our basic pseudocode, the first and most basic statement to learn is the `DISPLAY(expression)` statement. This statement will evaluate the `expression` to a single value, and then it will display that value to the user. In our "mental model" of a computer, this means that the value is printed on the user interface somewhere. The word `DISPLAY` is an example of a keyword in pseudocode, since it has a special meaning as part of the `DISPLAY(expression)` statement.

For example, the simplest program we can write is the classic "Hello World" program, which simply displays the message `"Hello World"` to the user. In pseudocode, that program would look like this:

```tex
DISPLAY("Hello World")
```

Notice that the `expression` part of the statement contains `"Hello World"` in quotation marks? That is because `"Hello World"` is text, so we should put it in quotes and make it into a string in our code. Also, since the string `"Hello World"` can be treated like a value, we can also say it is an expression, and therefore we can use it in the `expression` part of the statement. This may seem pretty straightforward now, but as our programs become more complex it is important to think about what pieces of code can be treated as values, expressions, and statements. 

So, in our "mental model" of a computer, pretend we are using a blank box as our user interface. It might look something like this:

```tex

```

Now, we can run our "Hello World" program in our "mental model" and see what it does. After we run that program, our user interface will now look like this:

```tex
Hello World
```

Awesome! We've just run our first imaginary program! If you look at the output, you might notice something strange - the text on our user interface doesn't include the quotation marks `""` that the expression `"Hello World"` contained. When we display text to the user, we'll remove the quotation marks from the beginning and the end of the string, and just display the text inside. Pretty handy!

Each time we run our program, we'll assume we are starting with an empty user interface. This makes it easy for us to make sure any programs we've previously run on our "mental model" won't interfere with the output of the current program. So, anytime we run the "Hello World" program, even if we run it multiple times back-to-back, our user interface will always look like this:

```tex
Hello World
```

So, now that we have that part down, let's look at creating some more complex programs using this `DISPLAY(expression)` statement.
