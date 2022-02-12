---
title: "Python If-Else"
pre: "5. "
weight: 50
date: 2021-02-11T00:00:01-05:00
---

{{< youtube >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Python also supports another kind of conditional statement, the **if-else statement**. Just like in pseudocode, an if-else statement contains a single Boolean expression, but two blocks of code. If the Boolean expression evaluates to `True`, then one block of statements is executed. If it is `False`, then the other block will be executed. 

The general structure of an if-else statement in Python is shown below:

```python
if <boolean expression>:
    <block of statements 1>
else:
    <block of statements 2>
```

Notice that the `else` keyword is followed by a colon, just like the first line of the if-else statement. As we'd expect, the first block of statements is executed if the `<boolean expression>` portion is `True` and the second block is executed if it is `False`. 

Once again, let's go through a couple of code traces using Python Tutor to explore how an if-else statement works in Python.

## Code Tracing Example - True

Here's a simple Python program that contains an if-else statement:

```python
def main():
    x = int(input("Enter a number: "))
    if x >= 0:
        print("Your number is positive!")
    else:
        print("Your number is negative")
    print("Thanks for playing!")


main()
```

This program accepts an input from the user, converts it to an integer, and then determines if the integer is a positive or negative number. Let's go through this program a couple of times in Python tutor to see how it works. As always, you can click this [Python Tutor](https://pythontutor.com/visualize.html#code=def%20main%28%29%3A%0A%20%20%20%20x%20%3D%20int%28input%28%22Enter%20a%20number%3A%20%22%29%29%0A%20%20%20%20if%20x%20%3E%3D%200%3A%0A%20%20%20%20%20%20%20%20print%28%22Your%20number%20is%20positive!%22%29%0A%20%20%20%20else%3A%0A%20%20%20%20%20%20%20%20print%28%22Your%20number%20is%20negative%22%29%0A%20%20%20%20print%28%22Thanks%20for%20playing!%22%29%0A%0A%0Amain%28%29&cumulative=false&curInstr=0&heapPrimitives=nevernest&mode=display&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false) link:

We'll start with the usual default state:

![Tutor 1](/cc110/images/lab7/tutor6_1.png)

Like always, Python will find the `main()` function and add it to the objects list. Then, it will call the `main()` function, and we'll be presented with an input prompt as shown here:

![Tutor 4](/cc110/images/lab7/tutor6_4.png)

Let's assume that the user inputs the string `"5"` here. That means that the integer value $5$ will be stored in the variable named `x`:

![Tutor 5](/cc110/images/lab7/tutor6_5.png)

Now we've reached the if-else statement. So, we'll need to evaluate the Boolean expression `x >= 0`. Since `x` is currently storing the value $5$, this expression will evaluate to `True`. Therefore, we'll move into the first block of statements in the if-else statement:

![Tutor 6](/cc110/images/lab7/tutor6_6.png)

From here, we'll print the message that the user's input was a positive number, as well as the goodbye message at the end of the program. It will entirely skip the second block of statements in the if-else statement, as we can see here:

![Tutor 7](/cc110/images/lab7/tutor6_7.png)

A full execution of this program is shown in the animation below:

![Tutor Gif 1](/cc110/images/lab7/tutor6_1.gif)

## Code Tracing Example - False

What if the user inputs a negative value, such as $-7$? In that case, we'll be at this state in our program:

![Tutor 10](/cc110/images/lab7/tutor6_10.png)

From here, we'll evaluate the Boolean expression `x >= 0` again. This time, however, we'll see that it evaluates to `False`, so we'll jump down to the second block of statements inside the if-else statement:

![Tutor 11](/cc110/images/lab7/tutor6_11.png)

This will print a message to the user that the input was a negative number, and then it will print the goodbye message. We completely skipped the first block of statements:

![Tutor 12](/cc110/images/lab7/tutor6_12.png)

A complete run through this program is shown in this animation:

![Tutor Gif 2](/cc110/images/lab7/tutor6_2.gif)

So, as we expect, an if-else statement allows us to run one block of statements or the other, based on the value of the Boolean expression. It is a very powerful piece of code, and it allows us to write programs that perform different actions based on the input provided by the user or the values of other variables. 

{{% notice note note-1 "What About Elif?" %}}

Python also includes another keyword `elif` that is used to chain together multiple if-else statements. We'll cover that topic in a future lab. For now, we won't need it to complete any of this lab's activities.

{{% /notice %}}
