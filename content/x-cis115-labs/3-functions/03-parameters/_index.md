---
title: "Parameters"
pre: "3. "
weight: 30
date: 2021-01-07T00:00:01-05:00
---

{{< youtube REDDx8L1eaU >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

The last new concept we're going to introduce in this lab is the concept of **parameters**. We just learned how to create procedures in our code, but our current understanding of procedures has one very important flaw in it: a procedure will always do the same thing each time we call it! What if we want to write a procedure that performs the same operation, but uses different data each time? Wouldn't that be useful?

Thankfully, we can do just that by introducing **parameters** into our procedures. A **parameter** is a special type of variable used in a procedure's code. The value of the parameter is not given in the procedure itself - instead, it is provided when the procedure is called. When a value is given as part of a procedure call, we call it an **argument**. So, a procedure has **parameters**, and the value of those parameters is given by **arguments** that are part of the procedure call. 

## Creating Procedures with Parameters

To include parameters as part of a procedure, we simply list the names of the parameters in the parentheses after the procedure name. If we want to use more than one parameter, we can separate them using a comma `,`. Here's an example of a `"Hello World"` procedure that uses two parameters:

```tex
PROCEDURE hello_world(first_name, last_name)
{
    DISPLAY("Hello ")
    DISPLAY(first_name)
    DISPLAY(" ")
    DISPLAY(last_name)
}
```

Inside of the procedure, we can use `first_name` and `last_name` just like any other variable. We can read the value stored in the variable by using it in an expression, and we can even change the value stored in the variable within the procedure itself using an assignment statement. 

## Calling a Procedure with Arguments

Now that we have a procedure that requires parameters, we need to call that procedure by providing arguments as part of the procedure call. To do that, we provide **expressions** that result in a value inside of the parentheses of a procedure call. Once again, multiple arguments are separated by commas.

For example, we can call the `hello_world` procedure by providing two arguments like this:

```tex
hello_world("Willie", "Wildcat")
```

So, when this code is run on our "mental model" of a computer, we should receive the following output on the user interface:

```tex
Hello Willie Wildcat
```

Let's walk through a quick code trace to see exactly what happens when we call a procedure with arguments.

## Code Tracing a Procedure with Arguments

First, let's formalize the example above into a complete program:

```tex
PROCEDURE hello_world(first_name, last_name)
{
    DISPLAY("Hello ")
    DISPLAY(first_name)
    DISPLAY(" ")
    DISPLAY(last_name)
}

PROCEDURE main()
{
    hello_world("Willie", "Wildcat")
}

main()
```

To do that, we've placed our procedure call in a `main` procedure, and we've added a call to the `main` procedure at the end of our program. So, once again, we can set up our code trace structure to include our code and the various boxes we'll use to keep track of everything:

![Trace Line 1](/images/lab2/trace5_1.png)

We are already pretty familiar with how our "mental model" of a computer will scan through the whole program to find the procedures, so let's skip ahead to the last line with the procedure call to `main`:

![Trace Line 5](/images/lab2/trace5_5.png)

Once again, our computer will see that it is calling the `main` procedure, which it knows about. So, it will jump to the beginning of the `main` procedure and start from there:

![Trace Line 6](/images/lab2/trace5_6.png)

This line contains another procedure call, this time to the `hello_world` procedure. However, when our "mental" computer looks up that procedure in its list of procedures, it notices that it requires a couple of parameters. So, our computer will also need to check that the procedure call includes a matching argument for each parameter. In our pseudocode language, each parameter must have a matching argument provided in the procedure call, or else the computer will not be able to run the program. 

Thankfully, we see that there are two arguments provided, the values `"Willie"` and `"Wildcat"`, which match the two parameters `first_name` and `last_name`. So, the procedure call is valid and we can jump to the beginning of the procedure.

![Trace Line 7](/images/lab2/trace5_7.png)

This time, however, we'll need to perform one extra step. When we call a procedure that includes parameters, we must also list the parameters as variables when we start the procedure. The value of those variables will be the matching argument that was provided as part of the procedure call. So, the parameter variable `first_name` will store the value `"Willie"`, and the parameter variable `last_name` will store the value `"Wildcat"`. Therefore, our code trace should really look like this when we start running the `hello_world` procedure:

![Trace Line 8](/images/lab2/trace5_8.png)

In the future, we'll show that as just one step in our code trace. Once we are in the `hello_world` procedure, we can simply walk through the code line by line and see what it does. At the end of the procedure, we'll see that it has produced the expected output:

![Trace Line 14](/images/lab2/trace5_14.png)

At this point, we will jump back to the `main` procedure. When we do this, there are a couple of other things that happen in our "mental model" of a computer:

1. Any variables created in the `hello_world` procedure are removed. This includes any parameter variables. 
1. We'll reset the code back to the original, removing any computed values and replacing them with the original expressions. 

So, after that step, our code trace should look like this:

![Trace Line 15](/images/lab2/trace5_15.png)

Now we are back in the `main` procedure, and the program will simply reach the end of that procedure, then jump back to the main procedure call and reach the end of the program. The full code trace is shown in the animation below:

![Trace 5](/images/lab2/trace5.gif)

That's all there is to calling a procedure that uses parameters! We can easily work through it using the code tracing technique we learned earlier in this lab.

{{% notice note note-3 "Parameter vs. Argument" %}}

The definitions for parameter and argument given above are the correct ones. However, many programmers are not very precise about how they use these terms, so in practice you may see the terms **parameter** and **argument** used somewhat interchangeably. 

We'll do our best to use them correctly throughout this course, and we encourage you to be careful about how you use the terms and make sure you understand the difference. 

{{% /notice %}}