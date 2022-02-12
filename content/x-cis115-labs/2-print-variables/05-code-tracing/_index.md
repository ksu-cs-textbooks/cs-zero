---
title: "Code Tracing"
pre: "5. "
weight: 50
date: 2021-01-07T00:00:01-05:00
---

{{< youtube kWd2mDYREg8 >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

As our programs become more complex, it can become more and more difficult to run them on our "mental model" of a computer without a little bit of help. So, let's go through an example of **code tracing**, one of the best ways to work through large blocks of code and keep track of everything that is going on. At the same time, we can also learn more about using variables in our programs!

## Multiple Variables

Our programs can also have multiple variables. In fact, there is no limit to the number of variables we can use - it just requires us to come up with a unique name for each one. For example, we could make a program that includes and displays multiple variables like this:

```tex
a <- "one"
b <- "two"
c <- "three"
d <- "four"
DISPLAY(a)
DISPLAY(" ")
DISPLAY(b)
DISPLAY(" ")
DISPLAY(c)
DISPLAY(" ")
DISPLAY(d)
```

This is a pretty complex program - one of the most difficult we've seen so far! To work out what it does, we can use a technique called **code tracing**. Let's see how it works!

## Code Tracing

Code tracing involves mentally walking through the code line by line and recording what each line does. So, we'll need to keep track of the current values of each variable, as well as the current output that is displayed to the user. We can easily do this by making a couple of boxes on a sheet of paper or in a couple of tabs of a text editor. For this example, we'll use a simple graphic like this one:

![Empty Trace](/cc110/images/lab2/trace1.png)

As we run the program, we'll keep track of which line of code we are on, and update the trace as we go. So, let's start by running the first line of code, `a <- "one"`. When we run this line, we'll need to create a new variable named `a` and store the value `"one"` in it. In our code trace, we can simply add an entry to the variables section as shown below:

![Trace Line 1](/cc110/images/lab2/trace2.png)

There is no right or wrong way to record variables in our code trace. We can use boxes for each value and update it as we go, or just write a short text entry as shown in our example. Any method is valid. In the meantime, we're using an arrow to keep track of which line we are running in our program, but we can just as easily do so with a finger or other tool in the real world!

Looking at the next three lines of code, we see that they are all similar. So, we can quickly run them and populate the next four entries in our variables box:

![Trace Line 2-4](/cc110/images/lab2/trace5.png)

Now we've reached the first `DISPLAY(expression)` statement in our program. If we recall the way those statements work, we should first evaluate the expression into a value. In our code, our expression is the variable `a`, which **isn't** a value. So, we need to evaluate it by looking up the current value of `a` and placing it in the current line of code. Then, we can display that value in the output. So, once we've run that line of code, our code trace will look something like this:

![Trace Line 5](/cc110/images/lab2/trace6.png)

The next line of code is just `DISPLAY(" ")`, which is simple since the expression `" "` is just a string value that doesn't need to be evaluated. So, we'll need to add a space to the end of our output. This can be tricky, since we really can't "see" spaces. For now, we'll just place a dash `-` in that space until we get the next piece of output. 

![Trace Line 6](/cc110/images/lab2/trace7.png)

Now we are back to a line that contains a variable. So, once again we look at the current value of the variable, place it in the expression, and then update our output. Since we've now received more output, we can remove that dash to make it a bit clearer. 

![Trace Line 7](/cc110/images/lab2/trace8.png)

From here on out, it should be pretty simple to figure out how the rest of this trace goes. When we are finished, we should have a code trace that looks like this:

![Final Trace](/cc110/images/lab2/trace12.png)

The whole process is shown below in animated form:

![Trace Animation](/cc110/images/lab2/trace.gif)

Code tracing is a great way to train our "mental model" to work just like a real computer. While this may seem like a slow and tedious process right now, remember all of the other things we've learned how to do. Reading is initially very difficult, but with time and practice we can go from recognizing individual letters, to sounding out words, and finally reading with ease! The same happens as we learn to program and read code - with practice we'll be able to do this in our head quickly and easily!