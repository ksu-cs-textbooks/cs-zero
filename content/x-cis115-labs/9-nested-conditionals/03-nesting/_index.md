---
title: "Nesting Conditionals"
pre: "3. "
weight: 30
date: 2021-03-16T00:00:01-05:00
---

{{< youtube TpYqzdioI7w >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

We've already seen how we can chain conditional statements by placing a new conditional statement inside of the `False` branch of another conditional statement. If we think about that, however, that implies that we probably should be able to place conditional statements inside of the `True` branch as well, or really anywhere. As it turns out, that's exactly correct. We call this **nesting**, and it is really quite similar to what we've already seen in this lab. 

Using nested conditional statements, we can really start to rethink the entire structure of our program and greatly simplify the code. Let's take a look at how we can do that with our Rock Paper Scissors game.

## Nesting Conditional Statements

In our Rock Paper Scissors game, we are really checking the value of two different variables, `p1` and `p2`. In all of our previous attempts, we built complex Boolean expressions that checked the values of both variables in the same expression, such as `p1 == "rock" and p2 == "scissors"`. What if we simply checked the value of one variable at a time, and then used nested conditional statements in place of the `and` operator? What would that look like?

Here's an example of a Rock Paper Scissors game that makes use of nested conditional statements:

![Nested Conditionals](/images/lab9/nested.svg)

Here, we begin by checking if the value in `p1` is `"rock"`. If it is, then we'll go to the `True` branch, and start checking the values of `p2`. If `p2` is also `"rock"`, then we know we have a tie and we can output that result. If not, we can check to see if it is `"paper"` or `"scissors"`, and output the appropriate result. If none of those are found, then we have to output an error.

In the `False` branch of the first conditional statement, we know that `p1` is not `"rock"`, so we'll have to check if it is `"paper"` and `"scissors"`. Inside of each of those conditional statements, we'll also have to check the value of `p2`, so we'll end up with a significant number of conditional statements in total!

Let's see what such a program would look like in Python:

```python
def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")

    if p1 == "rock":
        if p2 == "rock":
            print("tie")
        elif p2 == "paper":
            print("player 2 wins")
        elif p2 == "scissors":
            print("player 1 wins")
        else:
            print("error") 
    elif p1 == "paper":
        if p2 == "rock":
            print("player 1 wins")
        elif p2 == "paper":
            print("tie")
        elif p2 == "scissors":
            print("player 2 wins")
        else:
            print("error")
    elif p1 == "scissors":
        if p2 == "rock":
            print("player 2 wins")
        elif p2 == "paper":
            print("player 1 wins")
        elif p2 == "scissors":
            print("tie")
        else:
            print("error")
    else:
        print("error") 


main()
```

In this example, we have an outer set of chained conditional statements checking the value of `p1`, and then each of the branches will check the value of `p2` and determine which output is correct. It is very similar in structure to the chained conditional example on the previous page, just laid out a bit differently. As before, try running this program yourself in either Python or Python Tutor to make sure it works and you understand how it is structured. 

## Removing Duplicate States

Looking at this code, one thing we might quickly notice is that we now have four places that print `"error"` instead of just one. This is because we now have to check the values of `p2` in three separate places, and can't simply assume that the final `else` case in the outermost conditional statement is the only case where an error might be found.

One way we can simplify this code is by including a specific conditional statement just to check for any error situations, and handle those upfront before the rest of the code. So, we can rewrite this code as shown here to accomplish that:

```python
def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")

    if not (p1 == "rock" or p1 == "paper" or p1 == "scissors") or not (p2 == "rock" or p2 == "paper" or p2 == "scissors"):
        print("error")
    else:
        if p1 == "rock":
            if p2 == "rock":
                print("tie")
            elif p2 == "paper":
                print("player 2 wins")
            else:
                print("player 1 wins")
        elif p1 == "paper":
            if p2 == "rock":
                print("player 1 wins")
            elif p2 == "paper":
                print("tie")
            else:
                print("player 2 wins")
        else:
            if p2 == "rock":
                print("player 2 wins")
            elif p2 == "paper":
                print("player 1 wins")
            else:
                print("tie")


main()
```

By confirming that both `p1` and `p2` only contain either `"rock"`, `"paper"`, or `"scissors"` first, we can then make some pretty handy assumptions later in our code. For example, now the outermost conditional statement only explicitly checks if `p1` contains `"rock"` or `"paper"`, and then the third block is simply an `else` clause by itself. We can do this because we already know that `"scissors"` is the only other possible value that can be stored in `p1`, so we don't have to explicitly check for it. We can make similar changes to the nested conditional statements as well. So, just by adding one complex Boolean expression and conditional statement to our program, we were able to remove 4 that we no longer needed!

## Further Simplification

In fact, we can even take this one step further. Now that we know that both `p1` and `p2` only contain valid values, we can easily determine if that match has ended in a tie by simply checking if the variables contain the same value. So, with a bit of restructuring, we can simplify our program as shown here:

```python
def main():
    p1 = input("Enter 'rock', 'paper', or 'scissors' for player 1: ")
    p2 = input("Enter 'rock', 'paper', or 'scissors' for player 2: ")

    if not (p1 == "rock" or p1 == "paper" or p1 == "scissors") or not (p2 == "rock" or p2 == "paper" or p2 == "scissors"):
        print("error")
    else:
        if p1 == p2:
            print("tie")
        elif p1 == "rock":
            if p2 == "paper":
                print("player 2 wins")
            else:
                print("player 1 wins")
        elif p1 == "paper":
            if p2 == "rock":
                print("player 1 wins")
            else:
                print("player 2 wins")
        else:
            if p2 == "rock":
                print("player 2 wins")
            else:
                print("player 1 wins")


main()
```

This code presents a clear, easy to read version of a Rock Paper Scissors program. At the top, we receive input from the users, and then the first conditional statement is used to determine if the input is valid. If not, it will print an error. 

If the input is valid, then we can make some assumption about the various possible inputs in our program's logic, which greatly reduced the number of conditional statements. We are also checking for ties at the beginning, so in the `False` branch of that conditional statement we can also assume that the values in `p1` and `p2` are different, further reducing the number of items we have to check.

We'll revisit this example later in this course to show how we can convert the first conditional statement into a loop, which will prompt the user for new input if an invalid input is provided. This will make our program even better and easier for anyone to use. 