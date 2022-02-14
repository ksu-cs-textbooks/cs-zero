---
title: "Python If"
pre: "4. "
weight: 40
date: 2021-02-11T00:00:01-05:00
---

{{< youtube J0Zv4807Quw >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Boolean expressions in Python can be used in a variety of ways. One of the most important things we can do with a Boolean expression is affect the **control flow** of our program using a **conditional statement**.

Recall that a **conditional statement** is a type of statement that allows us to choose to run different pieces of code based on the value given in a Boolean expression. The simplest conditional statement is the **if statement**. 

In an **if statement**, we include a Boolean expression and a block of statements. If the Boolean expression evaluates to `True`, then we execute the code in the block of statements. If it is `False`, then we skip the block and continue with the rest of the program.

The structure of an if statement in Python is shown below:

```python
if <boolean expression>:
    <block of statements>
```

In this structure, we still have a `<boolean expression>` that is evaluated. However, instead of it being in parentheses like in pseudocode, in Python those parentheses are not required. After the Boolean expression is a colon `:`, just like at the end of a function definition. 

Then, the `<block of statements>` is included below the if statement's first line, and it must be indented one level. Again, this is very similar to the structure of a function definition in Python. In Python, the `<block of statements>` must include at least one line of code, otherwise Python won't be able to understand it. 

Let's go through a couple of code tracing examples in Python Tutor to see how an if statement works in code.

## Code Tracing Example - False

Consider this program in Python:

```python
def main():
    x = int(input("Enter a number: "))
    if x == 7:
        print("That's a lucky number!")
    print("Thanks for playing!")


main()
```

We can run that code in Python Tutor by clicking this [Python Tutor](https://pythontutor.com/visualize.html#code=def%20main%28%29%3A%0A%20%20%20%20x%20%3D%20int%28input%28%22Enter%20a%20number%3A%20%22%29%29%0A%20%20%20%20if%20x%20%3D%3D%207%3A%0A%20%20%20%20%20%20%20%20print%28%22That's%20a%20lucky%20number!%22%29%0A%20%20%20%20print%28%22Thanks%20for%20playing!%22%29%0A%0A%0Amain%28%29&cumulative=false&curInstr=0&heapPrimitives=nevernest&mode=display&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false) link. At first, our window should look something like this:

![Tutor 1](/images/lab7/tutor5_1.png)

When we step through the program, the first thing it will do is record the `main()` function in the objects list, as shown here:

![Tutor 2](/images/lab7/tutor5_2.png)

Then, we'll reach the call to the `main()` function, so Python Tutor will jump to that function and create a frame for all the variables needed:

![Tutor 3](/images/lab7/tutor5_3.png)

The next line of code will ask the user to input a number, so Python Tutor will show an input box at the bottom of the window:

![Tutor 4](/images/lab7/tutor5_4.png)

For this first time through the program, let's assume the user inputs the string `"42"` as input. So, when we click Submit, we'll see the integer value $42$ stored in the variable `x` in the `main` frame:

![Tutor 5](/images/lab7/tutor5_5.png)

At this point, we've reached the if statement. The first step is to evaluate the Boolean expression `x == 7`. Since `x` is actually storing the value $42$, this statement will evaluate to `False`. So, when we click the Next button on the state below:

![Tutor 6](/images/lab7/tutor5_6.png)

We'll see that the program arrow jumps past the block of statements in the if statement. So, the next line will simply print the goodbye message:

![Tutor 7](/images/lab7/tutor5_7.png)

Finally, the `main()` function will return, and we'll end the program:

![Tutor 8](/images/lab7/tutor5_8.png)

The entire process is shown in the animation below:

![Tutor 1 Gif](/images/lab7/tutor5_1.gif)

As we can see, when the Boolean expression evaluates to `False`, we'll just skip the block of statements inside of the if statement. This is the same result that we observed when we were working in pseudocode. 

## Code Tracing Example - True

Now let's see what happens when the Boolean expression evaluates to `True` instead. To see that, we can go back to the point where our program is asking for input, as shown below:

![Tutor 4](/images/lab7/tutor5_4.png)

This time, we'll assume the user inputs the string `"7"` as input. So, when we click Submit, we'll see the integer value $7$ stored in the variable `x` in the `main` frame:

![Tutor 9](/images/lab7/tutor5_9.png)

This time, when we reach the if statement, we'll see that the Boolean expression `x == 7` will evaluate to `True`. So, when we click the Next button, we'll be taken to the block of statements inside of the if statement:

![Tutor 10](/images/lab7/tutor5_10.png)

Here, we'll print the special message for finding a lucky number:

![Tutor 11](/images/lab7/tutor5_11.png)

Then, we'll print the program's goodbye message:

![Tutor 12](/images/lab7/tutor5_12.png)

And finally we'll reach the end of the `main()` function, so it will return and we'll be at the end of the program:

![Tutor 13](/images/lab7/tutor5_13.png)

The entire process can be seen in this animation:

![Tutor 2 Gif](/images/lab7/tutor5_2.gif)

So, when the Boolean expression evaluates to `True`, we'll run the code inside the if statement. If it is `False`, then we'll just skip past the if statement and continue with the rest of our program. 