---
title: "Input with Loops"
pre: "3. "
weight: 30
date: 2021-03-16T00:00:01-05:00
---

{{< youtube 4p1GqlPD36E >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

One of the most powerful features of loops is to deal with invalid user input. For example, if we want a user to input a positive number, but they accidentally input a negative number instead, what should our program do? Previously, all we could do was print an error and ask the user to run the program again, but that isn't very user friendly or efficient. Instead, we can use a loop to repeatedly prompt the user for input until we receive a valid input. 

Let's look at an example to see how this works. Consider the following pseudocode procedure:

```tex
PROCEDURE positive_input()
{
    DISPLAY("Enter a positive number: ")
    x <- NUMBER(INPUT())
    REPEAT WHILE(x <= 0)
    {
        DISPLAY("Invalid Input!\n")
        DISPLAY("Enter a positive number: ")
        x <- NUMBER(INPUT())
    }
    RETURN x
}
```

This procedure will prompt the user for input, and then store whatever is received in the variable `x`. However, if the user inputs a number that is less than or equal to $0$, it will print an error message and prompt the user for input once again. Let's quickly code trace through this procedure to see how it works.

## Code Trace

When code tracing a procedure, we simply start as if we are calling the procedure from somewhere else. So, our setup will look like this:

![Trace 1](/images/lab10/trace12_1.png)

This program begins by prompting the user for input, and then storing the input as a number in the variable `x`. So, let's assume that the user input the string `"-5"` when prompted. So, that will store the value $-5$ in the variable `x`.

![Trace 2](/images/lab10/trace12_2.png)

At this point, we've reached the beginning of our loop, so we need to determine if the Boolean expression evaluates to `true` or `false`. Since the value stored in `x` is less than or equal to $0$, the Boolean expression is `true` and we should enter the loop.

![Trace 3](/images/lab10/trace12_3.png)

Inside the loop, we know that the most recent input from the user was invalid. So, we'll print an error message, followed by a new prompt for input, and then we can read a new value from the user. This time, let's assume the user has input the string `"0"`, so we'll store the value $0$ in the variable `x`.

![Trace 4](/images/lab10/trace12_4.png)

Now we've reached the end of the loop, so we must go back to the beginning of the loop and start over.

![Trace 5](/images/lab10/trace12_5.png)

Here, we can check the Boolean expression once again. Since `x` now stores the value $0$, it is still less than or equal to $0$, so we should enter the loop again.

![Trace 6](/images/lab10/trace12_6.png)

Just like before, we'll print an error and then prompt the user for new input. This time, let's assume the user inputs the string `"7"`, so we'll store the value $7$ in the variable `x`.

![Trace 7](/images/lab10/trace12_7.png)

We're at the end of the loop once again, so now we'll jump back to the beginning of the loop.

![Trace 8](/images/lab10/trace12_8.png)

Here, we can test the Boolean expression yet again. This time, however, since `x` is not less than or equal to $0$, the Boolean expression is `false` and we can jump past the loop.

![Trace 9](/images/lab10/trace12_9.png)

At the bottom of the procedure, we are returning the value we received as input from the user. So, the value returned by this procedure will be $7$, which is a valid input that we received from the user itself. A full animation of this procedure is shown here.

![Trace Animation](/images/lab10/trace12.gif)

## Reading Input

Once we've created a procedure such as this in our programs, we can easily use it to read input from the user and verify that it meets the requirements we need. For example, consider this `main()` procedure that uses the `positive_input()` procedure we created above:

```tex
PROCEDURE main()
{
    a <- positive_input()
    b <- positive_input()
    c <- (a + b) / 2
    DISPLAY("The midpoint is " + c)
}
```

This program will simply find the midpoint between two positive numbers. All of the code for handling user input is in the `positive_input()` procedure, and we can call it multiple times to get multiple different inputs from the user. 

The `positive_input()` procedure is a great example of a simple **design pattern** that is commonly used in programs. A design pattern is simply a structure in code that is used to solve a particular problem, usually one that comes up often in many different programs. If we learn to solve these little problems by using these common programming structures, or patterns, it makes it much easier for others to read and understand our code. In addition, by learning these design patterns ourselves, it makes it much easier for us to solve common problems in our code - we can simply apply the relevant design pattern instead of trying to create a new solution from scratch. So, feel free to make use of the `positive_input()` procedure shown here, or adapt it as needed, anytime you need to read input from a user. 