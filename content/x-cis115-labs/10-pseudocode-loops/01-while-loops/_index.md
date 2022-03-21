---
title: "While Loops"
pre: "1. "
weight: 10
date: 2021-03-16T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

The first type of loop we'll explore in pseudocode is the **while loop**. A **while loop** is an iteration statement that will constantly repeat the code inside of it _while_ a Boolean expression evaluates to `true`. This is very similar to how an if statement is constructed - we know that the code inside an if statement is only executed if the associated Boolean expression is `true`. In the case of a while loop, we do basically the same thing, but at the end of the code inside the loop, we go back to the top and check the Boolean expression again. If it is still `true`, then we execute the code inside it over and over until it evaluates to `false`.

In pseudocode, the basic structure of a while loop is shown here:

```tex
REPEAT WHILE(<boolean expression>)
{
    <block of statements>
}
```

When we encounter a while loop, we first evaluate the `<boolean expression>` inside the parentheses to see if it is `true`. If so, we enter the loop and execute all of the code in the `<block of statements>` between the curly braces `{}`. Once we've reached the end of the block, where the closing curly brace `}` is found, we then **go back to the top** and evaluate the `<boolean expression>` again. If it evaluates to `true`, we run the code inside the loop again. 

We keep doing this until the `<boolean expression>` evaluates to `false`. As soon as it does, we jump down to the code immediately following the closing curly brace `}` at the end of the loop - we **don't** execute the code inside the loop again. 

This also means that when we initially reach the loop, we could run into the situation where the `<boolean expression>` evaluates to `false` the first time we see it. In that case, we just jump to the end of the loop and start executing the code after the closing curly brace `}`. There is no guarantee that we'll ever execute the code inside the loop, just like in an if statement.

## Code Tracing Example

To understand how a while loop works in practice, let's code trace an example program. Consider the pseudocode program shown here:

```tex
PROCEDURE main()
{
    DISPLAY("Enter a number: ")
    x <- NUMBER(INPUT())
    y <- 1
    REPEAT WHILE(y <= x / 2)
    {
        IF(x MOD y = 0)
        {
            DISPLAY(x + " is divisible by " + y + "\n")
        }
        y <- y + 1
    }
}

main()
```

Before we run a code trace on this program, take a moment to read it and see if you can guess what it does!

As always, we'll start our code trace by reviewing the code and keeping track of variables and procedures, as well as output. So, our initial setup will look like this:

![Trace 1](/images/lab10/trace10_1.png)

As we scan through the program, we'll find the `main()` procedure and record it in our list of procedures. 

![Trace 2](/images/lab10/trace10_2.png)

At the bottom of the program, we'll find a call to the `main()` procedure, so we'll jump to that procedure's code and start executing it.

![Trace 3](/images/lab10/trace10_3.png)

The first two lines of the `main()` procedure simply prompt the user for input and then store that input in the variable `x`. In this example, let's assume the user inputs the string `"12"` as input. So, we'll store the number $12$ in the variable `x`

![Trace 5](/images/lab10/trace10_5.png)

Next, we'll store the value $1$ in the variable `y`.

![Trace 6](/images/lab10/trace10_6.png)

At this point, we've reached the start of our loop. So, first we need to determine if the Boolean expression inside of the parentheses is `true` or `false`. Looking at the expression, it is checking if the value in `y` is less than or equal to half of the value stored in `x`. Since `x` is currently storing $12$, we know that half of `x` is $6$. Because `y` is only storing $1$, we know that `y` is definitely less than or equal to $6$, and the Boolean expression evaluates to true. Therefore, we should enter the loop and start executing the code inside.

![Trace 7](/images/lab10/trace10_7.png)

Inside of the loop, we find an if statement. So, we must determine if the Boolean expression inside of the if statement is `true` as well. In this case, we are checking if the remainder of dividing `x` by `y` is $0$ using the `MOD` operator. This is the same as checking to see if `x` can be evenly divided by `y`. Since `y` is currently $1$, we know that any integer divided by $1$ is itself with no remainder. So, this Boolean expression will evaluate to `true` and we should execute the code inside the if statement.

![Trace 8](/images/lab10/trace10_8.png)

Here, we find a `DISPLAY()` statement, so we'll just add that to our output and then exit the if statement below.

![Trace 9](/images/lab10/trace10_9.png)

Below the if statement, we see a simple assignment statement that will increase, or **increment**, the value of `y` by $1$. So, the variable `y` is now storing the value $2$.

![Trace 10](/images/lab10/trace10_10.png)

At this point, we've reached the end of the while loop. So, we need to loop back up to the beginning of the loop and start over again.

![Trace 11](/images/lab10/trace10_11.png)

Here, we need to once again evaluate the Boolean expression inside of the while loop. Since the value of `y` has changed, it might be different this time. However, we see that the $2$ store in `y` is still less than or equal to half of the value $12$ stored in `x`, so we enter the loop again.

![Trace 12](/images/lab10/trace10_12.png)

Inside the loop, we repeat the same process as before. We start by evaluating the Boolean expression inside of the if statement. Since $12$ is evenly divisible by $2$, that expression is `true` and we should enter the if statement.

![Trace 13](/images/lab10/trace10_13.png)

So, once again we'll print some output to the terminal:

![Trace 14](/images/lab10/trace10_14.png)

And then we'll leave the if statement and increment the value stored in `y` by $1$. 

![Trace 15](/images/lab10/trace10_15.png)

We're at the bottom of the loop, so we'll need to repeat by going back to the top once again.

![Trace 16](/images/lab10/trace10_16.png)

Hopefully by this point we have a pretty good idea of how this loop is working. We first check to see that $3$ stored in `y` is less than or equal to half of the value in `x`. Since it is, we'll continue the loop, and in the if statement inside we'll find that $12$ is evenly divisible by $3$, so we'll print some output, increment `y` by $1$, and loop back to the top. So, after that whole iteration, we should see the following in our code trace:

![Trace 17](/images/lab10/trace10_17.png)

With small, simple loops like this one, once we know what it does, we can typically just treat the whole loop like a single statement in our mental model of a computer. We know that it will increment the value of `y` each time, and if the value of `x` is equally divisible by `y`, it will print some output. Finally, we know we should keep repeating this step until `y` is greater than half the value of `x`. In many cases, we can simply refer to each iteration of the loop by the values of the variables used in the loop itself. So, after the iteration where `y` is equal to $4$, we'll see this state:

![Trace 18](/images/lab10/trace10_18.png)

Likewise, after the iteration where `y` is $5$, we'll see this state:

![Trace 19](/images/lab10/trace10_19.png)

Notice that this iteration did not produce any output, since $12$ is not evenly divisible by $5$. At this point, `y` is storing the value of $6$. Since that is exactly half of $12$, it still makes the Boolean expression `true` so we should execute the code in the loop again. After that iteration, we'll see the following state:

![Trace 20](/images/lab10/trace10_20.png)

At this point, `y` is now storing the value $7$. Since $7$ is not less than or equal to half of $12$, the Boolean expression inside the while loop will evaluate to `false` and we'll jump down to the bottom of the loop.

![Trace 21](/images/lab10/trace10_21.png)

Since there is no more code in the `main()` procedure, we'll return back to where the procedure was called, and then we'll see that we're at the end of the program! An entire trace of the program is shown in this animation.

![Trace 10 Animated](/images/lab10/trace10.gif)

As we can see, this program will determine all of the possible factors of the value that is provided by the user as input, and it will print them one at a time to the output. 

## While Loop Flowchart

Another way to visualize a while loop is using a flowchart. The pseudocode program above can be represented as the following flowchart:

![While Flowchart](/images/lab10/while_flow.svg)

In this flowchart, we once again begin at the top at the circle labeled "Start". From there, we see that our program will read input and store it in the variable `x`. We also create the variable `y` and store the initial value of $1$ there. At this point, we hit a diamond-shaped decision node, representing the while loop. If the Boolean expression in that decision node is `true`, then we follow the branch to the right that enters the loop. Here, we see yet another decision node that represents the if statement inside of the loop. When we see a loop and an if statement side by side in a flowchart like this, it is very easy to see how similar they actually are.

After the if statement, we increment the value stored in `y`, and then we see the flowchart path will loop back up to the beginning of the while loop, starting with the decision node at the top. This is the key concept in a while loop - once we reach the end of an iteration, we must go back to the top and enter the decision node once again. 

When we reach a point where the Boolean expression evaluates to `false`, our flowchart will then finish at the circle labeled "End".

So, just like we saw with conditional statements, using flowcharts is another great way we can try to understand the control flow in our programs. Feel free to make use of any of these tools as we continue to develop more complex programs in this course. 

{{% notice note note-1 "Repeat While vs. Repeat Until" %}}

In the [Official AP Pseudocode](https://apcentral.collegeboard.org/pdf/ap-computer-science-principles-exam-reference-sheet.pdf), the `REPEAT WHILE` loop is instead replaced with a `REPEAT UNTIL` loop. The concept is the same, except that the loop will repeat **until** the Boolean expression is `true`, instead of **while** the Boolean expression is `true`. We feel it is worth highlighting this change, since it does deviate from the official standard.

This is a very subtle change, and it is easy to translate between the two by simply adding a Boolean `NOT` operator to the Boolean expression. However, we chose to introduce loops using `REPEAT WHILE` instead of `REPEAT UNTIL` because most programming languages, including Python, only use while loops. There are few, if any, modern languages that use an "until" loop, and we feel that it adds an unnecessary complication to our pseudocode language. So, we've chosen to stick more closely to Python's loop structures than the ones introduced in the AP Pseudocode.

{{% /notice %}}