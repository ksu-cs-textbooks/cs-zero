---
title: "Testing Loops"
pre: "4. "
weight: 40
date: 2021-03-16T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Now that we've seen many examples of how to use loops in our code, let's briefly discuss some techniques for testing programs that contain loops. Many of these techniques are similar to ones we've explored when testing conditional statements, but there are a few important nuances to think about. 

## Branch and Path Coverage

First, just like we explored with conditional statements, it is important to test our programs in a way that we execute every possible branch, and try to find every possible path through the program as well. When dealing with a loop, usually we just consider two paths - one where the loop is entered at least once, and one where the loop is skipped entirely, if possible. 

Consider this example program in pseudocode:

```tex
PROCEDURE main()
{
    x <- NUMBER(INPUT())
    y <- NUMBER(INPUT())
    REPEAT WHILE(x < y)
    {
        x = x + x
    }
    DISPLAY(x)
}
```

This program will repeatedly double `x` until it larger than `y`. So, let's come up with some inputs for this program that achieve branch and path coverage. 

### Branch Coverage

To achieve branch coverage, we must simply come up with a set of inputs that will execute every line of code in the procedure at least once. So, let's try inputting $3$ and $5$ first. Since `x` is less than `y`, we enter the loop at least once. Eventually, `x` will become greater than `y`, so we'll exit the loop as well at some point. Therefore, we can say that the inputs `3` and `5` are enough to achieve branch coverage.

### Path Coverage

In this sample program, we've already executed all of the code, but we may want to try and come up with a set of inputs that will bypass the loop completely. This helps us check to make sure there aren't any issues with the code if the loop isn't executed at all. For this instance, consider the inputs `5` and `3`. In this case, the value in `x` is already greater than `y`, so the program will never execute the code inside of the loop at all. Thankfully, this doesn't break anything, so we know this program will work just fine without executing the loop.

## Loop Termination

When testing code that contains a loop, there is one other test we must consider - is it possible to reach a situation where the loop will **never** terminate? That is, once we start executing code within the loop, is it possible to get stuck in the loop and then never actually complete the program? 

Therefore, we must think carefully about our loops and situations that might cause problems. For example, what if we provide the inputs `-5` and `-3` to the pseudocode program above? 

In that case, we'll enter the loop since $-5$ is less than $-3$, but once we've executed the code in the loop, we'll see that `x` is now storing $-10$! We've actually gotten further away from a situation where the loop will terminate, which is definitely not good. In fact, this loop will repeat infinitely, and our program will run forever. 

So, we should either rethink our program a bit, or possibly add additional code to make sure the user does not input a negative value for `y`. By properly testing our program, we were able to discover a situation where the loop would not terminate!

{{% notice note note-1 "Proving Loop Termination" %}}

Unfortunately, it can be difficult to definitively prove if a loop will terminate in all cases. In computer science, we typically use a special concept known as a **loop variant** in order to prove that a loop will eventually terminate. Loosely, a loop variant is a way of expressing a maximum number of possible iterations of a loop before it terminates based on the current state of the program.

In the example above, we could say that our loop variant is the difference between `x` and `y`. Then, as long as we can show that the difference between those two values is monotonically decreasing each time the loop iterates, we can show that eventually it will reach a $0$ or less than $0$ and the loop will terminate. If the loop variant does not decrease, then the loop will not terminate. 

In this course, you won't be expected to reach that level of detail, but hopefully you'll be able to use some simple logic and common sense to figure out if a loop will terminate or if there are situations where it won't work correctly.

{{% /notice %}}