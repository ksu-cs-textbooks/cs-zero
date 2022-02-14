---
title: "Variables in Expressions"
pre: "6. "
weight: 60
date: 2021-01-07T00:00:01-05:00
---

{{< youtube A8pLZsIk69U >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Let's look at one more difficult concept in programming - using variables in the expressions for other variables. Right now we haven't learned any operators (don't worry - we'll cover those in great detail in a future lab), but it is still important for us to understand what happens when we use the value in one variable to create or update the value in another variable.

Let's consider this program:

```tex
x <- "Hello"
y <- x
DISPLAY(y)
DISPLAY(" ")
x <- "World"
DISPLAY(x)
DISPLAY(", ")
DISPLAY(y)
```

To work out what this program displays, we can once again use code tracing to work through it line by line. The first line is pretty easy - we see that we are simply storing the string value `"Hello"` in a new variable named `x`, so we can easily update that on our code trace as shown below:

![Trace Line 1](/images/lab2/trace2_1.png)

The next line is tricky - here we are storing the expression `x` into the variable named `y`. As before, we first have to evaluate the expression `x` to a value, which is simply the value stored in that variable. So, in actuality, we are storing the string value `"Hello"` in the variable `y` as well. 

**This is important to understand!** In the code, and indeed in our "mental model" of a computer, we might start to think that the values stored in variable `x` and `y` are connected somehow. However, this is not the case. What the line `y <- x` says is simply that `y` now stores **a copy** of the value that was stored in `x` **when this line is run**. Going forward, these two values are not connected in any way, as we'll soon see.

So, after running the second line of code, our code trace should now look like this:

![Trace Line 2](/images/lab2/trace2_2.png)

The next two lines are pretty simple, since they only display the value stored in `y` followed by a space. So, after running those two lines, we should see the following on our code trace:

![Trace Line 3-4](/images/lab2/trace2_4.png)

Now we reach the most important line, `x <- "World"`. When we run this line, we'll update the value stored in `x` to be the string value `"World"`. However, this **will not change** the value stored in `y`. This is because `y` stores a **copy** of the value that was previously stored in `x`, and any changes to the value stored in `x` will not impact the value stored in `y` at all. So, after running that line, our code trace should show the following:

![Trace Line 5](/images/lab2/trace2_5.png)

Once we've done that, running the next three lines of code is pretty straightforward. We'll just display the current value stored in in `x` and `y`, with a comma and space between them. So, at the end, our code trace should look like this:

![Trace Line 6-8](/images/lab2/trace2_8.png)

The entire trace can be seen in the animation below:

![Animated Trace](/images/lab2/trace2.gif)

As we have learned, code tracing is a very important skill, and it helped us discover one of the most important rules about working with variables: when we assign the value of one variable into another, we **copy** the existing value, but those two variables are not related to each other after the fact. 