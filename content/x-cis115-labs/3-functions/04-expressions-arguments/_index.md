---
title: "Expressions as Arguments"
pre: "4. "
weight: 40
date: 2021-01-07T00:00:01-05:00
---

{{< youtube hoGAf12Wng4 >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Let's briefly consider one more important situation that may arise when calling procedures. What if the arguments provided in a procedure call are variables themselves? What does that look like?

Let's work through an example:

```tex
PROCEDURE swap(one, two)
{
    temp <- one
    one <- two
    two <- temp
    DISPLAY(one)
    DISPLAY(two)
}

PROCEDURE main()
{
    first <-  "Willie"
    last <- "Wildcat"
    swap(first, last)
    DISPLAY(first)
    DISPLAY(last)
}

main()
```

Before reading the code trace below, take a moment to read this code and see if you can predict what the output will be.

## Code Tracing Expressions as Arguments

Like before, let's set up our code trace to include our code and the various boxes we need to keep track of everything:

![Trace Line 1](/cc110/images/lab2/trace6_1.png)

Let's go ahead and skip to the bottom where the `main` procedure call is. When we reach that line, we'll start at the top of the `main` procedure, like this:

![Trace Line 6](/cc110/images/lab2/trace6_6.png)

Next, we can move through the following two lines of code, which create the variables `first` and `last`, storing the values `"Willie"` and `"Wildcat"`, respectively. At this point, we're ready to call the `swap` procedure:

![Trace Line 8](/cc110/images/lab2/trace6_8.png)

To make a procedure call, we must first make sure the computer knows about the procedure. Since it is in our procedures box, we know we've seen it. The next step is to check and make sure that there is a matching argument for each parameter. The `swap` procedure requires two parameters, and we've provided two arguments, so that checks out. The next step is to actually evaluate each of the expressions used as arguments to a single value. If we look at our code, we see that the first argument expression is the variable `first`, which stores the value `"Willie"`. So, we can place that value where the variable goes in our procedure call:

![Trace Line 9](/cc110/images/lab2/trace6_9.png)

Then, we can do the same for the `last` variable, which stores the value `"Wildcat"`:

![Trace Line 10](/cc110/images/lab2/trace6_10.png)

Now that we've evaluated all of our argument expressions, we can finally perform the procedure call and enter the `swap` procedure. When we do this, we'll create two new variables, `one` and `two`, and populate them with the values that we evaluated for each expression. Just like when we store the value of one variable into another, these are **copies** of the values that were stored in the original variables. So, just because they have the same value, they otherwise aren't connected, as we'll see later. So, our current code trace should look like this:

![Trace Line 11](/cc110/images/lab2/trace6_11.png)

Inside of the `swap` procedure, we actually perform a three step "swap" process, which will swap the contents of the parameter variables `one` and `two`. First, we place the value of `one` in a new variable we call `temp`:

![Trace Line 12](/cc110/images/lab2/trace6_12.png)

Next, we place the original value in `two` into `one`. At this point, they both have the same value, but we've stored the original value from `one` into `temp`, so it hasn't been lost:

![Trace Line 13](/cc110/images/lab2/trace6_13.png)

Finally, we can place the value from `temp` into `two`, completing the swap:

![Trace Line 14](/cc110/images/lab2/trace6_14.png)

The next two lines will simply display the current values in `one` and `two` to the user:

![Trace Line 18](/cc110/images/lab2/trace6_18.png)

Notice that the values of `first` and `last` have not changed throughout this entire process. They are still the same values that were originally set in the `main` procedure. At this point, we've reached the end of the `swap` procedure. So, we can jump back to the location we left off in the `main` procedure. When we do so, we'll remove all of the variables we created in the `swap` procedure. We'll also reset all of the evaluated expressions in the `swap` procedure back to the original code. So, our code trace should now look like this:

![Trace Line 19](/cc110/images/lab2/trace6_19.png)

Since there's nothing else to evaluate on this line, we can move to the next line in the program:

![Trace Line 20](/cc110/images/lab2/trace6_20.png)

The next two lines are going to print the values of the `first` and `last` variables in the interface. Notice that, even though we swapped the values of `one` and `two` in the `swap` procedure, the values of `first` and `last` are unchanged here. This is an important concept to remember - when we use a variable as an argument in a procedure call, the procedure receives a copy of the value stored in that variable. So, any chagnes to the parameter variable in the procedure will not affect the variable that was used as an argument in the procedure call. In technical terms, we say this is a **call by value** procedure, since it uses the values in the arguments. 

So, after running those two lines of code, we should reach the end of the `main` procedure, and our code trace should look like this:

![Trace Line 24](/cc110/images/lab2/trace6_24.png)

At this point, we're at the end of the `main` procedure, so the computer will just jump back to the `main` procedure call, and reach the end of the program! The whole process is shown in the animation below:

![Trace 6](/cc110/images/lab2/trace6.gif)

As we can see, calling procedures is a pretty easy process. By using parameters, we can build procedures that repeat the same steps in our program, just with different data each time. 