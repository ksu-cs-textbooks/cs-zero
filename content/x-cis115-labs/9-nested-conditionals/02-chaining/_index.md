---
title: "Chaining Conditionals"
pre: "2. "
weight: 20
date: 2021-03-16T00:00:01-05:00
---

{{< youtube _gpasgFxlIw >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

In the previous example, we saw a set of linear if statements to represent a Rock Paper Scissors game. As we discussed on that page, the Boolean expressions are meant to be **mutually exclusive**, meaning that only one of the Boolean expressions will be true no matter what input the user provides. 

When we have mutually exclusive Boolean expressions like this, we can instead use if-else statements to make the mutually exclusive structure of the program clearer to the user. Let's see how we can do that.

## Chaining Conditional Statements

To chain conditional statements, we can simply place the next conditional statement on the `False` branch of the first statement. This means that, if the first Boolean expression is `True`, we'll execute the `True` branch, and then jump to the end of the entire statement. If it is `False`, then we'll go to the `False` branch and try the next conditional statement. Here's what this would look like in a flowchart:

![Chained Flowchart](/images/lab9/chain.svg)

This flowchart is indeed very similar to the previous one, but with one major change. Now, if any one of the Boolean expressions evaluates to `True`, that branch will be executed and then the control flow will immediately drop all the way to the end of the program, without ever testing any of the other Boolean expressions. This means that, overall, this program will be a bit more efficient than the one with linear conditional statements, because on average it will only have to try half of them before the program ends.

Now let's take a look at what this program would look like in Python:

```python
def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")

    if p1 == "rock" and p2 == "rock":
        print("tie")
    else:
        if p1 == "rock" and p2 == "paper":
            print("player 2 wins")
        else: 
            if p1 == "rock" and p2 == "scissors":
                print("player 1 wins")
            else:
                if p1 == "paper" and p2 == "rock":
                    print("player 1 wins")
                else:
                    if p1 == "paper" and p2 == "paper":
                        print("tie")
                    else:
                        if p1 == "paper" and p2 == "scissors":
                            print("player 2 wins")
                        else:
                            if p1 == "scissors" and p2 == "rock":
                                print("player 2 wins")
                            else:
                                if p1 == "scissors" and p2 == "paper":
                                    print("player 1 wins")
                                else:
                                    if p1 == "scissors" and p2 == "scissors":
                                        print("tie")
                                    else:
                                        if not (p1 == "rock" or p1 == "paper" or p1 == "scissors") and not (p2 == "rock" or p2 == "paper" or p2 == "scissors"):
                                            print("error")


main()
```

As we can see, this program is basically the same code as the previous program, but with the addition of a number of `else` keywords to place each subsequent conditional statement into the `False` branch of the previous one. In addition, since Python requires us to add a level of indentation for each conditional statement, we see that this program very quickly becomes difficult to read. In fact, the last Boolean expression is so long that it doesn't even fit well on the screen!

We can make a similar change to the other example on the previous page:

```python
def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")

    if (p1 == "rock" and p2 == "rock") or (p1 == "paper" and p2 == "paper") or (p1 == "scissors" and p2 == "scissors"):
        print("tie")
    else:
        if (p1 == "rock" and p2 == "paper") or (p1 == "paper" and p2 == "scissors") or (p1 == "scissors" and p2 == "rock"):
            print("player 2 wins")
        else:
            if (p1 == "rock" and p2 == "scissors") or (p1 == "paper" and p2 == "rock") or (p1 == "scissors" and p2 == "paper"):
                print("player 1 wins")
            else:
                if not (p1 == "rock" or p1 == "paper" or p1 == "scissors") and not (p2 == "rock" or p2 == "paper" or p2 == "scissors"):
                    print("error")


main()
```

Again, this results in very long lines of code, but it still makes it easy to see that the program is built in the style of mutual exclusion, and only one of the `True` branches will be executed. As before, feel free to run these programs directly in Python or using Python Tutor to confirm they work and that you understand how they work before continuing. 

## The Final Case

Now that we've built a program structure that enforces mutual exclusion, we'll might notice something really interesting - the final `if` statement is no longer required! This is because we've already exhausted all other possible situations, so the _only_ possible case is the last one. In that case, we can remove that entire statement and just replace it with the code from the `True` branch. Here's what that would look like in Python:

```python
def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")

    if p1 == "rock" and p2 == "rock":
        print("tie")
    else:
        if p1 == "rock" and p2 == "paper":
            print("player 2 wins")
        else: 
            if p1 == "rock" and p2 == "scissors":
                print("player 1 wins")
            else:
                if p1 == "paper" and p2 == "rock":
                    print("player 1 wins")
                else:
                    if p1 == "paper" and p2 == "paper":
                        print("tie")
                    else:
                        if p1 == "paper" and p2 == "scissors":
                            print("player 2 wins")
                        else:
                            if p1 == "scissors" and p2 == "rock":
                                print("player 2 wins")
                            else:
                                if p1 == "scissors" and p2 == "paper":
                                    print("player 1 wins")
                                else:
                                    if p1 == "scissors" and p2 == "scissors":
                                        print("tie")
                                    else:
                                        # All other options have been checked
                                        print("error")


main()
```

In this code, there is a comment showing where the previous if statement was placed, and now it simply prints an error. Again, this is possible because we've tried every possible valid combination of inputs in the previous Boolean expressions, so all that is left is invalid input. Try it yourself! See if you can come up with any valid input that isn't already handled by the Boolean expressions - there shouldn't be any of them. 

## Elif Keyword

To help build programs that include chaining conditional statements, Python includes a special keyword `elif` for this exact situation. The `elif` keyword is a shortened version of `else if`, and it means to replace the situation where an `if` statement is directly placed inside of an `else` branch. So, when we are chaining conditional statements, we can now do so without adding additional levels of indentation. 

Here's what the previous example looks like when we use the `elif` keyword in Python:

```python
def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")

    if p1 == "rock" and p2 == "rock":
        print("tie")
    elif p1 == "rock" and p2 == "paper":
        print("player 2 wins")
    elif p1 == "rock" and p2 == "scissors":
        print("player 1 wins")
    elif p1 == "paper" and p2 == "rock":
        print("player 1 wins")
    elif p1 == "paper" and p2 == "paper":
        print("tie")
    elif p1 == "paper" and p2 == "scissors":
        print("player 2 wins")
    elif p1 == "scissors" and p2 == "rock":
        print("player 2 wins")
    elif p1 == "scissors" and p2 == "paper":
        print("player 1 wins")
    elif p1 == "scissors" and p2 == "scissors":
        print("tie")
    else:
        # All other options have been checked
        print("error")


main()
```

There we go! That's much easier to read, and in fact it is much closer to the examples of linear conditionals on the previous page. This is the exact same program as before, but now it is super clear that we are dealing with a mutually exclusive set of Boolean expressions. And, we can still have a single `else` branch at the very end that will be executed if none of the Boolean expressions evaluates to `True`.

A structure of mutually exclusive statements like this is very commonly used in programming, and Python makes it very simple to build using the `elif` keyword. 

{{% notice note note-1 "Error Condition First" %}}

Using chained conditional statements like this makes it easy to detect and handle errors in the final `else` block, since all other options have already been checked. However, some programmers prefer to explicitly check for errors in the input at the start of the code, _before_ any other work is done. This is especially common when working with loops to prompt the user for new input in case of an error, which we'll learn about in a later lab.

When you are reading code, it is important to check both the start and end of a block of code when looking for possible error checks, since they could be included in either place. Recognizing common coding styles and conventions such as where to check for errors will help us better understand code written by others, and also make our code more readable by others.

{{% /notice %}}