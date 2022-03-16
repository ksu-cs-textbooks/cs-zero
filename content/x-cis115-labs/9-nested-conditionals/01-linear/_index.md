---
title: "Linear Conditionals"
pre: "1. "
weight: 10
date: 2021-03-16T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

To explore the various ways we can use conditional statements in code, let's start by examining the same problem using three different techniques. We'll use the classic [Rock Paper Scissors](https://en.wikipedia.org/wiki/Rock_paper_scissors) game. In this game, two players simultaneously make one of three hand gestures, and then determine a winner based on the following diagram:

![Rock Paper Scissors](/images/lab9/rps.svg)[^1]

[^1]: File:Rock-paper-scissors.svg. (2020, November 18). Wikimedia Commons, the free media repository. Retrieved 16:57, February 28, 2022 from https://commons.wikimedia.org/w/index.php?title=File:Rock-paper-scissors.svg&oldid=513212597.]

For example, if the first player displays a balled fist, representing **rock** and the second player displays a flat hand, representing **paper**, then the second player wins because "paper covers rock" according to the rules. If the players both display the same symbol, the game is considered a tie.

So, to make this work, we're going to write a Python program that reads two inputs representing the symbols, and then we'll use some conditional statements to determine which player wins. A basic skeleton of this program is shown below:

```python
def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")

    # determine the winner


main()
```

Our goal, therefore, is to replace the comment `# determine the winner` with a set of conditional statements and print statements to accomplish this goal.

## Linear Conditional Statements

First, let's try to write this program using what we already know. We've already learned how to use conditional statements, and it is completely possible to write this program using just a set of linear conditional statements and nothing else. So, to do this, we need to determine each possible combination of inputs, and then write an if statement for each one. Since there are $3$ possible inputs for each player, we know there are $3 * 3 = 9$ possible combinations:

| Player 1 | Player 2 | Output|
|:--------:|:--------:|:-----:|
| rock | rock | tie |
| rock | paper | player 2 wins |
| rock | scissors | player 1 wins |
| paper | rock | player 1 wins |
| paper | paper | tie |
| paper | scissors | player 2 wins |
| scissors | rock | player 2 wins |
| scissors | paper | player 1 wins |
| scissors | scissors | tie |

We also have to deal with a final option where one player or the other inputs an invalid value. So, in total, we'll have $10$ conditional statements in our program! 

Let's first try to make a quick flowchart of this program. Since we need $10$ conditional statements, our flowchart will have $10$ of the diamond-shaped decision nodes. Unfortunately, that would make a very large flowchart, so we'll only include the first three decision nodes in the flowchart shown here:

![Linear Flowchart](/images/lab9/linear.svg)

As we can see, this flowchart is very tall, and just consists of one decision node after another. Thankfully, we should know how to implement this in code based on what we've previously learned. Below is a full implementation of this program in Python, using just linear conditional statements:

```python
def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")

    if p1 == "rock" and p2 == "rock":
        print("tie")
    if p1 == "rock" and p2 == "paper":
        print("player 2 wins")
    if p1 == "rock" and p2 == "scissors":
        print("player 1 wins")
    if p1 == "paper" and p2 == "rock":
        print("player 1 wins")
    if p1 == "paper" and p2 == "paper":
        print("tie")
    if p1 == "paper" and p2 == "scissors":
        print("player 2 wins")
    if p1 == "scissors" and p2 == "rock":
        print("player 2 wins")
    if p1 == "scissors" and p2 == "paper":
        print("player 1 wins")
    if p1 == "scissors" and p2 == "scissors":
        print("tie")
    if not (p1 == "rock" or p1 == "paper" or p1 == "scissors") and not (p2 == "rock" or p2 == "paper" or p2 == "scissors"):
        print("error")


main()
```

This program seems a bit complex, but if we step through it one step at a time it should be easy to follow. For example, if the user inputs `"scissors"` for player 1 and `"rock"` for player 2, we just have to find the conditional statement that matches that input and print the correct output. Since we were careful about how we wrote the Boolean expressions for these conditional statements, we know that it is only possible for one of them to evaluate to true. So, we'd say that those Boolean expressions are **mutually exclusive**, since it is impossible for two of them to be true at the same time.

Things get a bit more difficult in the last conditional statement. Here, we want to make sure the user has not input an invalid value for either player. Unfortunately, the only way to do that using linear conditional statements is to explicitly check each possible value and make sure that the user did not input that value. This can seem pretty redundant, and it indeed is! As we'll see later in this lab, there are better ways we can structure this program to avoid having to explicitly list all possible inputs when checking for an invalid one.

Before moving on, it is always a good idea to run this code yourself, either directly in Python or using Python Tutor, to make sure you understand how it works and what it does. 

## Alternative Version

There is an alternative way we can write this program using linear if statements. Instead of having an if statement for each possible combination of inputs, we can instead have a single if statement for each possible output, and construct more complex Boolean expressions that are used in each if statement. Here's what that would look like in Python:

```python
def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")

    if (p1 == "rock" and p2 == "rock") or (p1 == "paper" and p2 == "paper") or (p1 == "scissors" and p2 == "scissors"):
        print("tie")
    if (p1 == "rock" and p2 == "paper") or (p1 == "paper" and p2 == "scissors") or (p1 == "scissors" and p2 == "rock"):
        print("player 2 wins")
    if (p1 == "rock" and p2 == "scissors") or (p1 == "paper" and p2 == "rock") or (p1 == "scissors" and p2 == "paper"):
        print("player 1 wins")
    if not (p1 == "rock" or p1 == "paper" or p1 == "scissors") and not (p2 == "rock" or p2 == "paper" or p2 == "scissors"):
        print("error")


main()
```

In this example, we now have just four if statements, but each one now requires a Boolean expression that includes multiple parts. So, this program is simultaneously more and less complex than the previous example. It has fewer lines of code, but each line can be much trickier to understand and debug.

Again, feel free to run this code in either Python Tutor or directly in Python to confirm that it works and make sure you understand it before continuing. 

In terms of style, both of these options are pretty much equivalent - there's no reason to choose one over the other. However, we'll see later in this lab, there are much better ways we can write this program using chaining and nesting with conditional statements.

{{% notice note note-1 "PEP 8 and Python Style" %}}

The Python programming language has its own style guide, known as "PEP 8" to most Python programmers. One of the major conventions proposed in that guide is limiting the length of each line of code to just 79 characters, in order to make the code more readable. However, as we've seen above, it is very easy to exceed that length when dealing with complex Boolean expressions, and we'll see this again as we add multiple levels of indentation when we nest conditional statements.

In this course, we won't worry about line length, even though some text editors may mark those lines as being incorrect in Python. Likewise, in many examples we won't wrap the lines to a shorter length, except for readability purposes in the videos and slides.

That said, it's definitely a good style to try and follow, and we encourage you to think about ways you can write your code to keep it as concise and readable as possible. Having shorter lines of code, while still using descriptive variable and function names, is a good start!

{{% /notice %}}