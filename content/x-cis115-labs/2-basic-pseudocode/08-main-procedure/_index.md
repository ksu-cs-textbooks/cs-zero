---
title: "Main Procedure"
pre: "8. "
weight: 80
date: 2021-01-07T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="slides" target="_blank">Slides</a>

Up to this point, we've simply written code and expected it to run easily in our "mental model" of a computer. However, many programming languages place one additional requirement on code that we should also follow: **all code must be part of a procedure**. 

What does this mean? Put simply, we shouldn't place any code in our programs that isn't part of a procedure. Or, put another way, our programs should only consist of procedures and nothing else.

But wait! Didn't we just learn that our "mental model" of a computer will just skip past procedures when it runs our programs, and it will only execute the code inside of a procedure when it is called? How can we call a procedure if all of our code must be within a procedure? It sounds a bit like a "chicken and egg" problem, doesn't it?

Thankfully, there is a quick and easy way to solve this. Many programming languages define one specific procedure name, usually `main`, as the defined starting point of a program. In those languages, the computer often handles calling the `main` procedure directly when a program starts. Other languages don't define this as a rule, but many developers choose to follow it as a convention. In our pseudocode, we will follow this convention, since this closely aligns with the Python language we'll learn later in the course. 

## Creating a Main Procedure

Let's see an example. We can update the example on the previous page to include a `main` procedure by simply placing all of the code at the bottom of the program into a procedure. We'll also include a call to the `main` procedure at the bottom of the code, as shown below:

```tex
PROCEDURE foo()
{
    DISPLAY("Run ")
}

PROCEDURE bar()
{
    DISPLAY("Forrest, ")
}

PROCEDURE main()
{
    foo()
    bar()
    foo()
}

main()
```

That's really all there is to it! From there, our "mental model" of a computer will know that it should start executing the program in the `main` procedure. Let's quickly code trace the first part of that process, just to see how it works. As before, we'll start running our program at the top of the code:

![Trace Line 1](/cc110/images/lab2/trace4_1.png)

Just like we saw previously, this line is creating a new procedure named `foo`. So, we'll make a note of that procedure, and move on to the next part of the code:

![Trace Line 3](/cc110/images/lab2/trace4_3.png)

Here, we are creating the `bar` procedure, so we'll record it and move on:

![Trace Line 5](/cc110/images/lab2/trace4_5.png)

Likewise, we see the creation of the `main` procedure, so we'll record it and continue working through the program:

![Trace Line 7](/cc110/images/lab2/trace4_7.png)

Finally, we've reached the end of the code, and here we see the call for the `main` procedure. So, just like we saw before, our "mental model" of a computer will determine that it has indeed seen the `main` procedure, and it will jump to the start of that procedure:

![Trace Line 8](/cc110/images/lab2/trace4_8.png)

From here, the rest of the program trace is pretty much the same as what we saw before. It will work through the code in the `main` procedure one line at a time, jumping to each of the other procedures in turn. Once it reaches the end of the `main` procedure, it will jump back to the bottom of the program where `main` is called, and make sure that there is nothing else to execute before reaching the end of the program. The full process is shown in the animation below:

![Trace 4](/cc110/images/lab2/trace4.gif)

**From here on out**, we'll follow this convention in our programs. Specifically:

1. All programs must contain a procedure named `main` as the starting point of the program.
1. All code in a program must be contained within a procedure, with the exception of a single call to the `main` procedure at the bottom of the program.

These conventions will help us write code that is easy to follow and understand. We'll also be learning good habits now that help us write code in a real programming language, such as Python, in a later lab.