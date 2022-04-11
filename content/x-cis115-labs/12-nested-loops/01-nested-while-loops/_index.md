---
title: "Nested While Loops"
pre: "1. "
weight: 10
date: 2021-04-10T00:00:01-05:00
---

{{< youtube jv4zWOMdLVA >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

To create a nested loop in Python, we can simply place a loop structure inside of the block of statements that is repeated by another loop structure. This is very similar to how we can nest conditional statements as well. 

For example, consider this short Python program:

```python
def main():
    i = 1
    while i < 10:
        j = i
        while j < 10:
            print("{} ".format(j), end="")
            j = j + 1
        print("")
        i = i + 1
    print("Complete!")


main()
```

In this example, we see a Python while loop that uses the variable `i` in its Boolean expression first, and then inside of that loop we see another loop that uses `j` in its Boolean expression. When we run this code, each time we execute the steps inside of the outer while loop, we'll have to completely go through the inner while loop as well. It can be very complex to keep track of everything, but with a bit of practice we'll learn some strategies for mentally working through loops.

Before continuing, take a look at that program's code and see if you can determine what it will print!

## Code Tracing Example

To really understand how a set of nested loops work, let's go through a code tracing example using Python Tutor. To follow along, place this code in the `tutor.py` file in the `python` folder on Codio, or click this [Python Tutor](https://pythontutor.com/visualize.html#code=def%20main%28%29%3A%0A%20%20%20%20i%20%3D%201%0A%20%20%20%20while%20i%20%3C%2010%3A%0A%20%20%20%20%20%20%20%20j%20%3D%20i%0A%20%20%20%20%20%20%20%20while%20j%20%3C%2010%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20print%28%22%7B%7D%20%22.format%28j%29,%20end%3D%22%22%29%0A%20%20%20%20%20%20%20%20%20%20%20%20j%20%3D%20j%20%2B%201%0A%20%20%20%20%20%20%20%20print%28%22%22%29%0A%20%20%20%20%20%20%20%20i%20%3D%20i%20%2B%201%0A%20%20%20%20print%28%22Complete!%22%29%0A%0A%0Amain%28%29&cumulative=false&curInstr=0&heapPrimitives=nevernest&mode=display&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false) link to load Python Tutor in a web browser.

When we first load this code in Python Tutor, we should see the following state:

![Tutor 1](/images/lab12/tutor9_1.png)

When we look at the bottom of the Python Tutor page, we'll see that we are on step 1 of 187 steps! That's a very large number of steps to deal with! Up to this point, most of our programs have been around 20 or 30 steps in total. So, already we're seeing that nested loops can quickly create programs that execute many more steps.

If we click next a few times, we'll see Python Tutor find the `main()` function definition, and then call that function from the bottom of the code. By the time we've entered the `main()` function, we should be at this state:

![Tutor 4](/images/lab12/tutor9_4.png)

Here, we are setting up the iterator variable `i` that is used for the outermost loop. So, we'll store the value $1$ in `i` and then move to the next line:

![Tutor 5](/images/lab12/tutor9_5.png)

Now we're at the start of our outer while loop. That means that we'll need to evaluate the Boolean expression and determine if it is `True` or `False`. In this case, we can see that `i < 10` will evaluate to `True`, so we should enter the loop.

![Tutor 6](/images/lab12/tutor9_6.png)

Once we are inside the loop, we'll start setting up the iterator variable `j` for the inner loop. In this code, we are storing the current value of `i` in `j`, so at this point `j` will also contain $1$.

![Tutor 7](/images/lab12/tutor9_7.png)

At this point, we need to decide if we should enter the inner while loop. So, once again we'll look at the Boolean expression, `j < 10`, and see that it is also `True` and we should enter the loop.

![Tutor 8](/images/lab12/tutor9_8.png)

Inside of the inner while loop, we'll perform two actions. First, we'll print the current value of `j` to the output, but we won't move to the next line since the `end` parameter is set to an empty string in the `print()` function:

![Tutor 9](/images/lab12/tutor9_9.png)

Then, we'll increment the value of `j` by $1$ before looping back to the top of the innermost loop:

![Tutor 10](/images/lab12/tutor9_10.png)

Notice that when we reach the end of the innermost loop, we jump back to the beginning of that loop, **NOT** to the beginning of the outermost loop. This is an important concept to learn - since we are only dealing with the inner loop at this point, we must continue to repeat its steps until the Boolean expression evaluates to `False`. So, since the Boolean expression `j < 10` still evaluates to `True`, we should enter the loop once again.

![Tutor 11](/images/lab12/tutor9_11.png)

Inside the loop, we'll print the current value of `j` to the same line of output as before:

![Tutor 12](/images/lab12/tutor9_12.png)

And once again we'll increment the value of `j` by $1$ and jump back to the top of the innermost while loop:

![Tutor 13](/images/lab12/tutor9_13.png)

Hopefully at this point we have a pretty good idea of what each step of the innermost while loop does. It will simply print the value of `j` and increment it by $1$, repeating those steps until `j` is greater than or equal to $10$. So, once the inner while loop terminates, we'll see this state:

![Tutor 35](/images/lab12/tutor9_35.png)

We jumped from step 13 to step 35 just to complete the inner while loop. Finally, at this point we'll print an empty string, which will move our output to the next line, and then we'll increment the value in `i` by $1$ before looping to the top of the outer while loop:

![Tutor 37](/images/lab12/tutor9_37.png)

Now we must check to see if we should enter the outer while loop again by checking the Boolean expression `i < 10`. Since that evaluates to `True`, we'll enter the loop a second time.

![Tutor 38](/images/lab12/tutor9_38.png)

Inside the loop, we'll reset the value of `j` to be the current value stored in `i`, which is now $2$, and then we'll reach the inner while loop:

![Tutor 39](/images/lab12/tutor9_39.png)

Here, we can evaluate the Boolean expression `j < 10`, which is currently `True`, and determine that we should enter the inner while loop.

![Tutor 40](/images/lab12/tutor9_40.png)

Inside the loop, the code hasn't changed, so we can use our understanding from before to quickly figure out what this loop does. It will print the current value in `j` and then increment `j` by $1$, so we'll end up at this state:

![Tutor 42](/images/lab12/tutor9_42.png)

At this point, we can easily assume that the inner loop will do pretty much the same thing as before - it will print all of the values from `i` up through $9$ to the output, all on the same line. So, once the inner loop has completely finished, we'll see the following state in Python Tutor:

![Tutor 64](/images/lab12/tutor9_64.png)

We were able to quickly jump from step 42 all the way to step 64 just by understanding what the inner loop is doing and extrapolating from our previous experience. Now, we can finish up this iteration of the outer loop by printing a newline and then incrementing `i` by $1$, and then we'll be back at the beginning of the outer while loop:

![Tutor 66](/images/lab12/tutor9_66.png)

At this point, we've completely worked through two iterations of the outermost while loop, including two complete executions of the innermost while loop. So, we're at a good point to make a prediction about the output of the program as a whole, without executing the next 120 steps. It looks like the inner loop will print the values from `i` through $9$ on a single line, and then each line will start with the value of `i` being incremented by $1$ each time. So, overall, we can expect the entire outer while loop to produce the following output:

```tex
1 2 3 4 5 6 7 8 9 
2 3 4 5 6 7 8 9 
3 4 5 6 7 8 9 
4 5 6 7 8 9 
5 6 7 8 9 
6 7 8 9 
7 8 9 
8 9 
9
```

And, indeed, if we jump ahead to the last line of the program we'll see exactly that situation in Python Tutor:

![Tutor 186](/images/lab12/tutor9_186.png)

The program ends by printing the string `"Complete!"`. At the end of the program, we'll see the following state:

![Tutor 187](/images/lab12/tutor9_187.png)

A full animation of this process is shown here. After the first full iteration of the outer while loop, the rest of the internal steps are omitted and only the end of each loop iteration is shown.

![Tutor 9 Animated](/images/lab12/tutor9.gif)

Working through an example program such as this one is a great way to explore how nested loops work in Python

## Tips for Nested Loops

Writing code that has nested while loops can be quite tricky, as there are several pitfalls that we might encounter. Here are a few tips to keep in mind when designing code that uses nested while loops:

1. Try to understand the relationship between each loop's Boolean expression. If possible, use different variables in each one. It is easy to write code where the Boolean expressions are closely related, causing an infinite loop to occur.
1. Consider moving the internal loop to a separate function. That way it can be tested independently by calling the function directly elsewhere in your code. 
1. Look for ways to combine the nested loops into a single loop if possible. While this may not always be an option, it can make reasoning about the code much simpler. 
1. Try to make the loops as simple as possible. It is much easier to debug loops that use a simple iterator that increments regularly instead of a complex Boolean expression. Likewise, try to build loops that either both increment or both decrement the iterator variable to maintain consistency.

Nested loops present a very difficult challenge for programmers, because they are short snippets of code that may end up resulting in hundreds or even thousands of individual steps to be executed. So, anything we can do to make the loops simpler and easier to understand will greatly improve our ability to write programs with fewer bugs. 