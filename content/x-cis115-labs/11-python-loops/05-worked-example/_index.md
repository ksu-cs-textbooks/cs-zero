---
title: "Worked Example"
pre: "5. "
weight: 50
date: 2021-03-16T00:00:01-05:00
---

{{< youtube 1MUxdVRemk4 >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Now that we've learned all about using loops in Python, let's go through a complete worked example to see how all the pieces fit together. As we continue to develop larger and more complex programs, it is helpful to observe the entire process from start to finish so we can see how to easily develop a program one step at a time. Once we've created our program, we'll also perform a bit of testing to make sure that it works correctly.

## Problem Statement

For this example, let's write a program to play a simple number guessing game. Here's how it works:

> The game will select two random numbers from $0$ to $100$, one for each player. Then, each player will guess a number in the range, and the game will print either "higher" if that player's secret number is larger than the guess, or "lower" if the player's secret number is smaller than the guess. Players will alternate turns until one player correctly guesses their secret number and wins the game.

This game is pretty simple, but there are still quite a few different parts that we need to build in order to write the entire program. So, let's go through the process of building a complete program in Python to play this game.

## Random Numbers

Before we start building our program, we need some way to generate a random number. Thankfully, Python has a built-in library called [Random](https://docs.python.org/3/library/random.html) that has many functions for working with random numbers in our programs.

To use a library in Python, we must first **import** it into our code. This is done using a simple `import` statement at the very top of our program's code, followed by the name of the library we want to use. So, for this library, we'll need to have the following `import` statement at the top of our source code:

```python
import random
```

Once we've done that, we can use the function `random.randint(a, b)` to generate a random number that is between `a` and `b`, inclusive. Mathematically, we can say that it generates an integer $x$ such that $a <= x <= b$.

So, here's a quick test program we can use to explore how to use random numbers in Python:

```python
import random


def main():
    a = int(input("Enter a minimum value: "))
    b = int(input("Enter a maximum value: "))
    x = random.randint(a, b)
    print("A random number between {} and {} is {}".format(a, b, x))


main()
```

Take a minute to run this program and modify it a bit to make sure you understand how to work with random numbers in Python before continuing.

## Basic Structure

In Python, we know that all of our programs must include a `main()` function and a call to the `main()` function, so we can start building our solution by creating that basic structure as shown here:

```python
def main()


main()
```

In the program itself, we need to start by generating two random numbers from $0$ to $100$, one for each player. So, we can create and store those numbers in the `main()` function, and we'll also need to import the `random` library at the top of our file. 

```python
import random


def main():
    p1_secret = random.randint(0, 100)
    p2_secret = random.randint(0, 100)


main()
```

Once we have the secret numbers, then we can sketch out the game itself. We'll use a while loop to repeat until a player has guessed correctly, and we'll also use a simple integer variable to keep track of the current player. Inside of the loop, we should get a new guess from a player, and also switch between players. So, let's add that to our program structure using some comments:

```python
import random


def main():
    p1_secret = random.randint(0, 100)
    p2_secret = random.randint(0, 100)
    player = 1
    while( ): # player has not guessed correctly
        # swap player
        # get new guess from player
        # check if secret is higher or lower


main()
```

From here, we can start to work on the actual logic in our program.

## Boolean Expression

The trickiest part of this program is coming up with the correct Boolean expression to use in our while loop. That helps us determine if the player has guessed correctly and that the loop should stop. However, this is a bit complex since there are two different players, each one with their own secret number. So, in our Boolean expressions, we have to determine what the current player is as well as whether the most recent guess was correct.

To do this, we can use the `and` and `or` Boolean operators to combine several Boolean expressions together. For example, we can determine if the current player is player 1 using `player == 1`, and then we can determine if the most recent guess is equal to player 1's secret number using `guess == p1_secret`. If we want both of those to be `True` in order to exit the loop, we can combine them using the `and` operator. We can do something very similar for player 2 as well. Then, if we want the loop to terminate if _either_ of those is true, we can combine the two statements using the `or` operator.

So, all together, we want to repeat the loop as long as that entire statement is not `True`. So, the full Boolean expression would be:

```python
not ((player == 1 and guess == p1_secret) or (player == 2 and guess == p2_secret))
```

That's pretty complex, but it easily encompasses all of the rules of the game!

## Handling Input

To get input from the user, we can write a simple `read_input()` function that is very similar to the ones we saw earlier in this lab. We simply want to make sure the user has provided a value that is between $0$ and $100$, and prompt the user for another input if not. We'll also add in a parameter to print the current player in the prompt for input. 

So, our `read_input()` function might look something like this: 

```python
def read_input(player):
    x = int(input("Enter a guess for player {}: ".format(player)))
    while x < 0 or x > 100:
        print("Invalid Input!")
        x = int(input("Enter a guess for player {}: ".format(player)))
    return x
```

Then, in our `main()` function, we can simply use the new `read_input()` function to read a player's current guess as shown here:

```python
def main():
    p1_secret = random.randint(0, 100)
    p2_secret = random.randint(0, 100)
    player = 1
    while(not ((player == 1 and guess == p1_secret) or (player == 2 and guess == p2_secret))): # player has not guessed correctly
        # swap player
        guess = read_input(player)
        # check if secret is higher or lower


main()
```

## Checking Guess and Swapping Players

Next, we need to add some conditional statements to check if the secret is higher or lower than the guess, and also to swap between players. First, let's look at swapping players. This is pretty simple, since all we need to do is find out what the current player is, and switch that value to the other player. So, we can do that using a simple if statement as shown here:

```python
def main():
    p1_secret = random.randint(0, 100)
    p2_secret = random.randint(0, 100)
    player = 1
    while(not ((player == 1 and guess == p1_secret) or (player == 2 and guess == p2_secret))): # player has not guessed correctly
        if player == 1:
            player = 2
        else:
            player = 1
        guess = read_input(player)
        # check if secret is higher or lower


main()
```

The process for checking a guess is very similar - we can simply check to see if the guess is higher or lower than the secret for the current player, and print the output accordingly. First, we'll need to figure out the current player:

```python
if player == 1:
    # check player 1's secret
else:
    # check player 2's secret
```

Then, in each of those branches, we'll check the guess:

```python
if player == 1:
    if guess < p1_secret:
        print("Higher")
    elif guess > p1_secret:
        print("Lower")
    else:
        print("Correct!")
else:
    if guess < p2_secret:
        print("Higher")
    elif guess > p2_secret:
        print("Lower")
    else:
        print("Correct!")
```

This is a pretty straightforward set of conditional statements, but it goes to show how many lines of code are required even for a simple guessing-game program like this one.

## Initial Testing and Debugging

So, at this point, we can put all of the pieces together and test our program. Here is the complete program that we've written so far:

```python
import random


def read_input(player):
    x = int(input("Enter a guess for player {}: ".format(player)))
    while x < 0 or x > 100:
        print("Invalid Input!")
        x = int(input("Enter a guess for player {}: ".format(player)))
    return x


def main():
    p1_secret = random.randint(0, 100)
    p2_secret = random.randint(0, 100)
    player = 1
    while(not ((player == 1 and guess == p1_secret) or (player == 2 and guess == p2_secret))):
        if player == 1:
            player = 2
        else:
            player = 1
        guess = read_input(player)
        if player == 1:
            if guess < p1_secret:
                print("Higher")
            elif guess > p1_secret:
                print("Lower")
            else:
                print("Correct!")
        else:
            if guess < p2_secret:
                print("Higher")
            elif guess > p2_secret:
                print("Lower")
            else:
                print("Correct!")


main()
```

So, let's try to run this program and see if it works. Unfortunately, right from the start we have an error in our code, since when we try to execute this program, we'll get the following error:

![Error 1](/images/lab11/error1.png)

Take a minute to see if you can spot and fix the error before continuing!

Unfortunately, in our Boolean expression inside of the while loop, we're referencing the `guess` variable, but that variable isn't actually created until later inside the while loop itself. So, we'll need to set the `guess` variable to a value outside of the while loop first. 

Also, we must be very careful about what value we use. If we set `guess` to be $0$ initially, there is a very small chance that player 1 could win the game immediately if their secret number is $0$, since that is a valid guess. Instead, let's set `guess` to be $-1$ so that it will never be equal to a secret number.

After we make that change, when we run the program again, we may notice one other error:

![Error 2](/images/lab11/error2.png)

Can you spot it by looking at this screenshot? 

Unfortunately, our program starts with player 2's turn instead of player 1. Why is that? Well, if we look closely at our code, we see that we are initially setting the player to player 1, but then immediately switching players inside of the while loop before we prompt for input. If we think about it, we can't move the code that swaps players to later in the while loop, because then our Boolean expression to determine if the while loop should terminate will be incorrect. So, instead, we can simply initialize the `player` variable to be $2$, and then it will be switched to $1$ before we prompt for input the first time.

So, our final working program's code with these two changes is shown here:

```python
import random


def read_input(player):
    x = int(input("Enter a guess for player {}: ".format(player)))
    while x < 0 or x > 100:
        print("Invalid Input!")
        x = int(input("Enter a guess for player {}: ".format(player)))
    return x


def main():
    p1_secret = random.randint(0, 100)
    p2_secret = random.randint(0, 100)
    player = 2
    guess = -1
    while(not ((player == 1 and guess == p1_secret) or (player == 2 and guess == p2_secret))):
        if player == 1:
            player = 2
        else:
            player = 1
        guess = read_input(player)
        if player == 1:
            if guess < p1_secret:
                print("Higher")
            elif guess > p1_secret:
                print("Lower")
            else:
                print("Correct!")
        else:
            if guess < p2_secret:
                print("Higher")
            elif guess > p2_secret:
                print("Lower")
            else:
                print("Correct!")


main()
```

A full example of running this program, complete with a very lucky guess, is shown in the screenshot below:

![Correct 1](/images/lab11/correct1.png)

## Testing - Branch and Path Coverage

Now that we have a complete and working program, let's look at what it might take to test it. Unfortunately, testing a program that uses random numbers can be very tricky, since each time you run the program you might receive different outputs even if you provide the same inputs.

Thankfully, we can still perform some testing to achieve branch and path coverage by choosing our guesses carefully. Here are the basic methods we'll want to try:

* Guessing $0$ for each player should result in `"Higher"` for output, unless the secret number is $0$.
* Guessing $100$ for each player should result in `"Lower"` for output, unless the secret number is $100$.
* Guessing the same value for one player while actually playing the game for the other player will eventually result in an output of `"Correct"`. Using a bit of logic, it is always possible to win the game in no more than $7$ guesses. 
* Trying to input an invalid value should result in `"Invalid Input!"` for output at least once. 

Following those simple strategies and keeping track of the various outputs received, it is pretty easy to eventually test all branches and most, if not all, possible paths through the program. 

## Testing - Loop Termination

Checking for loop termination on this program is a bit trickier, since the secret numbers are random and the guesses that a player makes are also unpredictable. So, while we can't say for sure that the program will terminate, we can always prove that there is a possible condition where the loop will terminate, and that condition depends entirely on the user providing the correct input. So, as long as it is possible, we can say that the loop is at least not an infinite loop, and the program will work correctly if the user makes the correct guess.

There we go! We've just explored a complete example of writing a program in Python, complete with loops and conditional statements. We also introduced random numbers and how we can easily use those in our programs. Beyond that, we explored how to test these programs and correct minor errors found in testing. Hopefully this process is very helpful as we continue to work on larger and more complex programs.