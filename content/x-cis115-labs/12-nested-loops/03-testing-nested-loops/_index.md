---
title: "Testing Nested Loops"
pre: "3. "
weight: 30
date: 2021-04-10T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Testing nested loops can also be very tricky, especially because they can make our program's control flow even more complex. So, let's briefly go through an example to see how to determine what inputs we can use to test nested loops.

Consider the following example program:

```python
def positive_input():
    x = int(input("Enter a positive integer: "))
    while x <= 0:
        print("Invalid input!")
        x = int(input("Enter a positive integer: "))
    return x


def main():
    x = positive_input()
    y = positive_input()
    while y <= x:
        for i in range(x - y):
            print("*", end="")
            y = y + 2
        print("")
    print("Complete!")


main()
```

Let's work through the process of generating some test cases for this program to see if it runs without any errors. As always, our biggest concern is to make sure that we don't reach a situation where the program enters an infinite loop, and that we also try to provide inputs that will enter each loop at least once, and also bypass each loop if possible.

## Input Loop

First, we see that the `positive_input()` function uses a loop to make sure the user inputs only positive values. So, some of our first test cases could involve trying values such as $-1$, $0$ and $1$ to check the edge cases of that while loop's Boolean expression. When we run the program and provide those inputs, we should see it enter the loop in that function at least once.

![Output 2](/images/lab12/output2.png)

We can also bypass that loop by simply making sure we enter a positive integer each time. So, we know we have a few test cases available that will achieve branch coverage for that loop.

## Outer While Loop

Next, let's consider the outermost while loop in the `main()` function. That loop uses the Boolean expression `y <= x` to determine if the loop should be entered or not. So, we want to come up with a few tests that check the edge cases of that Boolean expression. We can start by choosing a value to use for `x`, such as $5$. Then, the edge cases of that Boolean expression would be when `y` is either $4$, $5$, or $6$. 

If `y` is $6$, the Boolean expression would be `False` and it should bypass the loop. We can easily test this to make sure that is the case:

![Output 3](/images/lab12/output3.png)

Likewise, if `y` is $4$, we know that it should enter the outermost loop. Inside, we see a for loop that will iterate based on the expression `x - y`. Effectively, it will compute the difference between `x` and `y` and then iterate that many times. So, if `x` is $4$ and `y` is $5$, the difference between those values will be $1$. So, we'll enter the innermost for loop at least once. When we run the program with these inputs, we'll see the following output:

![Output 4](/images/lab12/output4.png)

What if we set both `x` and `y` to be the same value? We know that the inner for loop will run `x - y` times, so if both `x` and `y` are the same value, this would be a way to bypass that loop, while still entering the outermost while loop since `y <= x` will be `True`. However, when we try to run the program with these inputs, we'll see something interesting happen:

![Output 5](/images/lab12/output5.png)

Our program will quickly start printing blank lines of output to the terminal. So quickly, in fact, that it is hard to even see what happens. As it turns out, we accidentally caused our program to enter an **infinite loop**! When this happens, the only way to stop the program is to close the terminal window it is running in, or use the CTRL+C keyboard command to interrupt it. So, let's see why this infinite loop is occurring, and figure out how we can fix it.

## Infinite Loop

Did you spot the infinite loop when you first read the program's code? It can be really tricky to find, which is why we have to be very good about choosing test cases that will explore many different ways to run the program.

In this case, the infinite loop is caused by the interaction between the two loops. In the outermost while loop, we have the Boolean expression `y <= x` to enter the loop. However, inside that loop, the for loop will only execute `x - y` times, which also happens to be the **loop variant** for the outer while loop. The key to the infinite loop lies in the fact that the **only** line inside of the outer while loop that will change the value of either `x` or `y` is also inside of the inner for loop. So, if we don't execute the for loop's code at all, then the value of `x` and `y` won't change either, and we'll continually repeat the steps of the outermost while loop.

There are many ways to fix this problem, but the simplest would be to change the Boolean expression of the outermost while loop to be `y < x`. That will ensure that there is at least one iteration of the innermost for loop, and the infinite loop condition will be avoided.

So, as this example shows, testing nested loops is just like testing regular loops - we want to try and find inputs that will enter the loop at least once, as well as inputs that will bypass the loops if possible, just to make sure there aren't any strange situations that may arise. While this won't find all errors that are present in code containing nested loops, it is a great way to start testing your programs. 