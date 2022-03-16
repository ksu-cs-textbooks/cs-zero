---
title: "Testing Loops"
pre: "4. "
weight: 40
date: 2021-03-16T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Another important aspect of working with loops in code is learning how to properly test programs that contain loops. So, let's look at some of the methods we can use when testing our programs containing loops to make sure they work correctly and won't run into any problems. 

## Branch and Path Coverage

Loops, like conditional statements, introduce different branches and paths into our programs. So, one of the first steps when testing these programs is to develop a set of inputs that will execute each branch of the code, as well as finding inputs that will execute multiple different paths through the program. Since loops may repeat many times, typically we only worry about two possible paths when dealing with loops - one path where it is skipped entirely and another path where the loop is entered at least once. 

Let's consider this simple Python program that contains loops:

```python
def main():
    x = int(input("Enter a number: "))
    y = int(input("Enter a number: "))
    i = 0
    line = ""
    while i < x + y:
        line = line + "*"
        print(line)
        i = i + 1
    while i > x - y:
        print("=", end="")
        i = i - 1
    print()


main()
```

This program will simply print a right triangle of asterisks `*` that is `x + y` characters wide and tall, similar to a previous example in this lab. However, it will also print a final line of equals signs `=` below that, consisting of `x - y` characters. To test this program, we want to try and find some input values for `x` and `y` that achieve branch and path coverage.

### Branch Coverage

To achieve branch coverage, we want to execute each line of code in this program at least once. An easy way to do that is to provide inputs so that the sum of `x` and `y` is a positive number in order to enter the first loop. After the first loop terminates, the value of `i` will be equal to the sum of `x` and `y`, provided that value is greater than $0$. So, in order to also enter the second loop, we need to make sure the difference of `x` and `y` is smaller than their sum. 

A set of inputs that achieves this would be $3$ and $1$ for `x` and `y`, respectively. Their sum is $4$, so the first loop will be executed 4 times. Then, the difference between the values is $2$, so the second loop will executed twice to reduce the value in `i` to $2$. 

So, we can say that the inputs `3` and `1` are enough to achieve branch coverage.

### Path Coverage

To achieve path coverage, we must consider three additional paths through the program:

1. Neither loop is entered
2. Only the first loop is entered
3. Only the second loop is entered

First, in order to enter neither loop, we must have a set of inputs where the sum is less than or equal to $0$, and also where the difference is less than or equal to $0$. The simplest way to achieve this is to set both inputs to exactly $0$! Sometimes the simplest inputs are the easiest for testing.

To enter the first loop only, we need the situation where the sum of `x` and `y` is greater than `0`, but then their difference is even larger. An easy way to accomplish this is to set `y` to a small negative number. For example, we could set `x` to $3$ and `y` to $-1$. That will make their sum $2$ but the difference $4$, so we'll only execute the first loop but not the second one. 

Finally, if we want to execute the second loop only, we need to make both the sum and the difference of `x` and `y` a number less than $0$. In that case, we can simply set both `x` and `y` to negative values, but make sure that `x` is overall a smaller value than `y`. So, we could set `x` to $-3$ and `y` to $-1$. In that case, their sum is $-4$ but their difference is $-2$. That will cause the program to skip the first loop but enter the second loop.

So, we can achieve path coverage with these four sets of inputs:

* `3, 1`
* `0, 0`
* `3, -1`
* `-3, -1`

## Loop Termination

When testing loops, we should also check to make sure that the loops will eventually terminate if we ever enter them. Thankfully, in this program, it is very easy to reason about this and convince ourselves that it works.

Consider the first loop - the only way to enter that loop is if the value of `i` is less than the sum of `x` and `y`, and each time the loop iterates the value in `i` will be incremented by $1$. Since `i` is getting larger each time, eventually it will reach a value that is greater than or equal to `x + y` and the loop will terminate.

The same argument can be made for the second loop. In that loop, `i` is initially greater than the difference of `x` and `y`, but `i` is decremented each time, so eventually the loop will terminate. 

Technically speaking, we can come up with a **loop variant** for each loop and show that it is monotonically decreasing. This is easily done by simply finding the difference between the iterator variable `i` and the termination condition of the loop, either the sum or the difference of `x` and `y`. We won't ask you to get to this level of detail when testing your own loops, but it is a very useful concept to understand when working with loops.

There we go! We were able to quickly come up with a set of inputs that will execute all possible branches and paths in this program, and we can also show that each of the loops will properly terminate anytime they are executed. So, we know that our program at least won't crash, no matter what integers are provided as input. We can also examine the output of each test and make sure that it matches what the expected output should be in order to show that our program not only doesn't crash, but that it provides the _correct_ output.  