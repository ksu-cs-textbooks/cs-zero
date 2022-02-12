---
title: "Pseudocode Testing"
pre: "3. "
weight: 30
date: 2021-02-11T00:00:01-05:00
---

{{< youtube >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

One important concept to understand when writing if statements and if-else statements is the **control flow** of the program. Before we learned about conditional statements, our programs had a linear control flow - there was exactly one pathway through the program, no matter what. Each time we ran the program, the same code would be executed each time in the same order. However, with the introduction of conditional statements, this is no longer the case.

Because of this, testing our programs becomes much more complicated. We cannot simply test it once or twice, but instead we should plan on testing our programs multiple times to make sure they work exactly the way we want. So, let's go through some of the various ways we can test our programs that include conditional statements.

## Example Program

First, let's consider this example pseudocode program:

```tex
PROCEDURE main()
{
    DISPLAY("Enter a number: ")
    x <- NUMBER(INPUT())
    DISPLAY("Enter another number: ")
    y <- NUMBER(INPUT())
    IF (x + y > 10)
    {
        DISPLAY("Branch 1")
    }
    ELSE
    {
        DISPLAY("Branch 2")
    }
    IF (x - y > 10)
    {
        DISPLAY("Branch 3")
    }
    ELSE
    {
        DISPLAY("Branch 4")
    }
}

main()
```

We can represent the two if-else statements in this pseudocode in the following flowchart as well:

![Control Flow Flowchart](/cc110/images/lab7/control.png)

## Branch Coverage

First, let's consider how we can achieve **branch coverage** by executing all of the branches in this program. This means that we should test the program using different sets of inputs that will run different branches in the code. Our goal is to execute the code in each branch at least once. In this example, we see that there are four branches, helpfully labeled with the numbers one through four in the `DISPLAY()` statements included in each branch. 

So, let's start with a simple set of inputs, which will store $6$ in both `x` and `y`. Which branches will be executed in this case? Before reading ahead, see if you can work through the code above and determine which branches are executed?

In the first if-else statement, we'll see the `x + y` is equal to $12$, which is greater than $10$, making that Boolean statement `true`. So, we'll execute the code in branch 1 this time through. When we reach the second if-else statement, we'll compute the value of `x - y` to be $0$, which is less than $10$. In this case, that makes the Boolean statement `false`, so we'll execute branch 4. Therefore, by providing the inputs `6` and `6`, we've executed the code in branches 1 and 4. 

So, can we think of a second set of inputs that will execute the code in branches 2 and 3? That can be a bit tricky - we want to come up with a set of numbers that add to a value less than $10$, but with a difference that is greater than $10$. However, we can easily do this using negative numbers! So, let's assume that the user inputs $6$ for `x` and $-6$ for `y`. When we reach the first if-else statement, we can compute the result of `x + y`, which is $0$. That is less than $10$, so the Boolean statement is `false` and we'll execute the code in branch 2. So far, so good!

Next, we'll reach the second if-else statement. Here, we'll compute the result of `x - y`. This time, we know that $6 - -6$ is actually $12$, which is greater than $10$. So, since that Boolean expression is `true`, we'll run the code in branch 3. That's exactly what we wanted!

Therefore, if we want to test this program and try to execute all the branches, we only have to provide two pairs of inputs:

* $6$ and $6$
* $6$ and $-6$

However, that's only one way we can test our program. There are many other methods we can follow!

## Path Coverage

A more thorough way to test our programs is to achieve **path coverage**. In this method, our goal is to execute all possible paths through the program. This means that we want to execute every possible ordering of branches! So, since our program has 4 branches in two different if-else statements, the possible orderings of branches are listed below:

1. Branch 1 -> Branch 3
2. Branch 1 -> Branch 4
3. Branch 2 -> Branch 3
4. Branch 2 -> Branch 4

As we can see, there are twice as many paths as there are branches in this case! We've already covered ordering 2 and 3 from this list, so let's see if we can find inputs that will cover the other two orderings.

First, we want to find a set of inputs that will execute branch 1 followed by branch 3. So, we'll need two numbers that add to a value greater than 10, but their difference is also greater than 10. So, let's try the value $12$ for `x` and $0$ for `y`. In that case, their sum is greater than $10$, so we'll execute branch 1 in the first if-else statement. When we reach the second if-else statement, we can evaluate `x - y` and find that it is also $12$, which is greater than $10$ and we'll execute branch 3. So, we've covered the first ordering!

The last ordering can be done in a similar way - we need a pair of inputs with a sum less than $10$ and also a difference less than $10$. A simple anwer would be to input $4$ for both `x` and `y`. In this case, their sum is $8$ and their difference is $0$, so we'll end up executing branch 2 of the first if-else statement, and branch 4 of the second if-else statement. So, that covers the last ordering.

As we can see, path coverage will also include branch coverage, but it is a bit more difficult to achieve. If we want to cover all possible paths, we should test our program with these 4 sets of inputs now:

* $6$ and $6$
* $6$ and $-6$
* $12$ and $0$
* $4$ and $4$

There's still one more way we can test our program, so let's try that out as well.

## Edge Cases

Finally, we should also use a set of inputs that test the "edges" of the Boolean expressions used in each if-else statement. An **edge** is a value that is usually the smallest or largest value before the Boolean expression's output would change. So, an **edge case** is simply a set of input values that are specifically created to be edges for the Boolean expressions in our code. 

For example, let's look at the first Boolean logic statement, `x + y > 10`. If we are simply considering whole numbers, then the possible edge cases for this Boolean expression are when the sum of `x + y` is exactly $10$ and $11$. When it is $10$ or below, the result of the Boolean expression is `false`, but when the result is $11$ or higher, then the Boolean expression is `true`. So, $10$ and $11$ represent the **edge** between `true` values and `false` values. The same applies to the Boolean expression in the second if-else statement.

So, to truly test the edge cases in this example, we should come up with a set of values with the sum and difference of exactly $10$ and exactly $11$. For the first one, a very easy solution would be to set `x` to $10$ and `y` to $0$. In this case, both the sum and the difference is $10$, so we're on the `false` side of the edge. Our program will correctly execute branches 2 and 4. 

For the other edge, we can use a similar set of inputs where `x` is $11$ and `y` is still $0$. In this case, both the sum and difference is $11$, so each Boolean expression will evaluate to `true` and we'll execute branches 1 and 3. 

Why is this important? To understand that, we must think a bit about what was intended by this program. What if the program should execute branches 1 and 3 if the value is greater than or equal to $10$? In that case, both of our chosen edge cases should execute branches 1 and 3, but instead we saw that the edge case $10$ executed branches 2 and 4 instead. This is a simple **logic error** that happens all the time in programming - we simply forgot to use the greater than or equal to symbol `>=` instead of the simple greater than symbol `>` in our code. So, a minor typo like that can change the entire execution of our program, and we wouldn't have noticed it in _any_ of our previous tests. This is why it is important to test the edge cases along with other inputs.

In fact, it would probably be a good idea to add a third edge case, where the sum and difference equal $9$, just to be safe. That way, we can clearly see the difference between `true` and `false` values in this program.

So, the final set of values we may want to test this program with are listed below:

* $6$ and $6$ (branch coverage 1 and 4)
* $6$ and $-6$ (branch coverage 2 and 3)
* $12$ and $0$ (path coverage 1 and 3)
* $4$ and $4$ (path coverage 2 and 4)
* $9$ and $0$ (edge case 2 and 4)
* $10$ and $0$ (edge case 2 and 4)
* $11$ and $0$ (edge case 1 and 3)

As we can see, even a simple program with just a few lines of code can require substantial testing to really be sure it works correctly! This doesn't even include other types of testing, where we make sure it works properly with invalid input values, decimal numbers, and other situations. That type of testing is really outside of the scope of this lab, but we'll learn more about some of those topics later in this course. 