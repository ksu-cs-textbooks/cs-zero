---
title: "For Loops"
pre: "2. "
weight: 20
date: 2021-03-16T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Another type of loop that is commonly used in programming is the **for loop**. Instead of a while loop, which only uses a Boolean expression to determine if a loop repeats, a for loop is typically used to iterate a defined number of times, either by counting up or by iterating across a data structure such as a list. We'll learn more about how to use for loops with lists later in this course. 

In pseudocode, a for loop is used to iterate a specific number of times. The basic syntax for a for loop is shown here:

```tex
REPEAT <n> TIMES
{
    <block of statements>
}
```

In this example, the placeholder `<n>` is used to represent a number, typically a positive integer, that gives the number of times the loop should be executed. Then, we will execute the statements in the `<block of statements>` the given number of times. Put another way, we can say that this loop will execute the `<block of statements>` **for** `n` times - this is why we call this a **for loop**.

## Code Tracing Example

Let's look at a quick example program to see how a for loop works in practice. Consider the following pseudocode program:

```tex
PROCEDURE main()
{
    DISPLAY("Enter a number: ")
    x <- NUMBER(INPUT())
    DISPLAY("Enter a number: ")
    y <- NUMBER(INPUT())
    z <- 1
    REPEAT y TIMES
    {
        z < z * x
    }
    DISPLAY(x " to the power of " y " = " z)
}

main()
```

Just like before, take a minute to read this program and see if you can determine how it works before continuing to the description below.

Once again, we'll begin by setting up or code tracing structure as shown here:

![Code Trace 1](/images/lab10/trace11_1.png)

First, we'll find the `main()` procedure, and record it in the list of procedures.

![Code Trace 2](/images/lab10/trace11_2.png)

Then, we'll encounter a call to the `main()` procedure, so we'll move our execution to the first line of code inside of that procedure.

![Code Trace 3](/images/lab10/trace11_3.png)

Here, the first two lines will prompt the user to input a number, and then that number will be stored in the variable `x`. For this example, let's assume the user inputs the string `"5"`, so the number $5$ will be stored in the variable `x`.

![Code Trace 4](/images/lab10/trace11_4.png)

Likewise, we'll do the same for the variable `y`. So, let's assume the user inputs `"3"`, which will store the number $3$ in the variable `y`.

![Code Trace 5](/images/lab10/trace11_5.png)

The program will also initialize the variable `z` by storing the number $1$ in it. 

![Code Trace 6](/images/lab10/trace11_6.png)

At this point, we've reached the for loop in our code. When we evaluate a for loop, we need to keep track of how many iterations are left. So, the easiest way to do that is to create a new hidden variable that is initially set to the value given for how many times to repeat the loop, and then we can count down using that variable. So, in our list of variables, we'll create a new variable `i` to keep track of the loop. It should initially store the same value that is stored in `y`, so we'll store $3$ in `i`.

![Code Trace 7](/images/lab10/trace11_7.png)

Now we are ready to see if we should enter the loop. Since `i` is greater than $0$, we know that we have at least one loop iteration to go. Therefore, we'll enter the loop.

![Code Trace 8](/images/lab10/trace11_8.png)

Inside the loop, we'll update the value stored in `z` by multiplying it by `x`. So, `z` will now store the value $5$.

![Code Trace 9](/images/lab10/trace11_9.png)

Now we've reached the end of the loop. At this point, we've completed a full iteration of the loop, so we can subtract $1$ from the hidden loop counter variable `i`. This is called **decrementing** a variable. Once we've done that, we can loop back up to the beginning of the loop itself.

![Code Trace 10](/images/lab10/trace11_10.png)

Here, we once again must check to see if we should enter the loop. Since our loop counter variable `i` is greater than $0$, we know that we can enter the loop again.

![Code Trace 11](/images/lab10/trace11_11.png)

Inside the loop, we'll oncea again update the value in `z` by multiplying it by `x`. So, `z` now stores $25$.

![Code Trace 12](/images/lab10/trace11_12.png)

Then, we'll reach the end of the loop, so we must decrement the value in `i` and jump back to the top of the loop.

![Code Trace 13](/images/lab10/trace11_13.png)

Since `i` is still greater than $0$, we'll enter the loop once again.

![Code Trace 14](/images/lab10/trace11_14.png)

We'll multiply the value in `z` by `x`, which means `z` will now be storing $125$.

![Code Trace 15](/images/lab10/trace11_15.png)

At the end of the loop, we'll decrement `i` again and return back to the top of the loop.

![Code Trace 16](/images/lab10/trace11_16.png)

At this point, we see that `i` is now equal to $0$. This means that we've executed the loop the correct number of times, we can now jump to the code after the loop.

![Code Trace 17](/images/lab10/trace11_17.png)

Finally, at the end of the program, we'll print the result of our calculation.

![Code Trace 18](/images/lab10/trace11_18.png)

Now that we've reached the end of the `main()` procedure, we'll return back to where it was called from. Since that is the end of the code, the program stops executing. A full animation of this program can be seen here.

![Code Trace Animation](/images/lab10/trace11.gif)

As we were able to show through code tracing, this program will compute the result of taking the first input to the power of the second input. Since the power operation is simply repeatedly performing multiplication a set number of times, it is easily done through the use of a for loop.