---
title: "Return in Procedures"
pre: "3. "
weight: 30
date: 2021-01-29T00:00:01-05:00
---

{{< youtube V7heqqfatCk >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Getting data from the user is one way we can store data in our programs. What if we want to create a procedure that produces a new data value? We can do that using a special statement called the **return** statement. 

In a procedure, we can choose any expression to be the result of calling the procedure, which will allow us to use the procedure as part of an expression instead of a statement. To really understand how this works, let's see it in action! Here's an example of a complete pseudocode program with a procedure that returns a value:

```tex
PROCEDURE mult_mod(value, multiply, modulo)
{
    value <- value * multiply
    value <- value MOD modulo
    RETURN(value)
}

PROCEDURE main()
{
    DISPLAY("Enter a value: ")
    text <- INPUT()
    value <- NUMBER(text)
    answer <- mult_mod(value, 5, 3)
    DISPLAY(answer)
}

main()
```

In the `mult_mod()` procedure, we see that the last line of code is `RETURN(value)`. This line will end the procedure, and it will use the current value stored in the `value` variable as the **return value** from the procedure. Then, in the `main()` procedure, we see that the procedure call for `mult_mod()` is actually part of an assignment statement `answer <- mult_mod(value, 5, 3)`. So, when the `mult_mod()` procedure is called, it will perform its work and then produce a return value, which can then be stored in the `answer` variable in the `main()` procedure. In effect, we can now use a procedure call to compute a value, which is a very useful thing in our programs. Let's work through a code trace using this code to see how it works.

## Code Trace

Like always, we'll start with the usual setup for our code trace as shown below.

![Trace 8 Step 1](/images/lab4/trace8_1.png)

The first few steps will simply find the procedures declared in the code. Once we reach the call to the `main()` procedure at the bottom, we should be at this state:

![Trace 8 Step 3](/images/lab4/trace8_3.png)

So, we'll enter the `main()` procedure. Here, we print a prompt to the user, and then accept input using the `INPUT()` expression:

![Trace 8 Step 5](/images/lab4/trace8_5.png)

In this example, let's assume the user inputs the number $7$ as input. So, we'll update our code trace to show that string value being stored in the `text` variable:

![Trace 8 Step 6](/images/lab4/trace8_6.png)

Next, we'll need to convert that string value to a numerical value using the `NUMBER()` procedure, storing that result in the `value` variable:

![Trace 8 Step 7](/images/lab4/trace8_7.png)

At this point, we are ready to call the `mult_mod()` procedure. So, we'll jump up to the first line of that procedure, and create a new set of variables that represent all of the parameters of the `mult_mod()` procedure, with values matching the arguments provided in the procedure call:

![Trace 8 Step 8](/images/lab4/trace8_8.png)

The first two steps of the `mult_mod()` procedure will multiply the `value` parameter by the `multiply` parameter, then find the modulo of that result and the `modulo` parameter. As it does so, it updates the value stored in the `value` variable. Once it is done, `value` should store the value $2$:

![Trace 8 Step 10](/images/lab4/trace8_10.png)

Now we've reached the `RETURN()` statement. This statement will end the `mult_mod()` procedure, so for this example it is the last line of code. Inside of the `RETURN()` statement, we are choosing to return the value stored in the `value` variable. So, in our variables list, we'll remove all of the variables from the `mult_mod()` procedure, but we'll place a special variable there showing the value that is being returned from the procedure. In our code trace, we'll just call that the `RETURN` variable:

![Trace 8 Step 11](/images/lab4/trace8_11.png)

Now, back in the `main()` procedure, we can deal with the assignment statement on the current line. Here, we will take the value returned from the `mult_mod()` procedure, which we see as the `RETURN` variable, and store that value in the `answer` variable in main. Once we've done that, our code trace will look like this:

![Trace 8 Step 12](/images/lab4/trace8_12.png)

Notice that the `RETURN` variable disappears once we've passed that line. The `RETURN` value is only used immediately after the procedure is called, to help evaluate the expression that it is a part of. Once that is done, the value is no longer needed.

Finally, we can complete the program by printing the answer to the output:

![Trace 8 Step 13](/images/lab4/trace8_13.png)

We'll reach the end of the `main()` procedure, and once we've moved back to the outer level of the code, we'll see that there is no more work to be done. The full trace is shown in this animation:

![Trace 8 Animation](/images/lab4/trace8.gif)

Returning values from a procedure is a really useful tool in programming. It allows us to create procedures that can perform a complex calculation for us, and then we can use those procedures in other expressions to perform even more complex calculations. It is all about finding ways to simplify our programs by creating small, repeatable pieces of code for each task. 