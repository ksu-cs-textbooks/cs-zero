---
title: "Worked Example"
pre: "5. "
weight: 50
date: 2021-03-16T00:00:01-05:00
---

{{< youtube 9N6fnhzND-E >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Let's go through a complete worked example program so we can see how to use loops to transform a problem statement into a working program. Once we're done, we'll also talk about how we can test the program to determine if it works correctly and won't run into an error.

## Problem Statement

For this example, we're going to write a simple program to play a variant of the game Nim known as the [21 Game](https://en.wikipedia.org/wiki/Nim#The_21_game). Here are the rules:

> The game begins with the first player choosing either $1$, $2$, or $3$. Then, the second player chooses either $1$, $2$ or $3$ and adds that number to the number chosen by the first player to establish a total. The game continues by alternating between players, each choosing to add either $1$, $2$ or $3$ to the total. The game is over when the total reaches $21$ or higher. The player who adds the number to the total that causes the game to end is the loser. 

This is a very simple game, and a great example of how loops can be used in a program in a variety of different ways. So, let's see what it takes to create this program.

## Basic Structure

To begin, we need to start with a `main()` procedure and a call to the `main()` procedure, as shown here:

```tex
PROCEDURE main()
{

}

main()
```

Next, we know that the program will repeat until the total is greater than or equal to $21$. So, we can easily add a variable to keep track of the total, and a loop that will represent the actual game being played.

```tex
PROCEDURE main()
{
    total <- 0
    REPEAT WHILE(total <= 21)
    {
        # players take turns
    }
    # game over
}

main()
```

We also need some way to keep track of which player's turn it is. So, we'll need a variable to track that, as well as a simple conditional statement at the end of our loop to switch between the two players. In pseudocode, that would look like this:

```tex
PROCEDURE main()
{
    total <- 0
    player <- 1
    REPEAT WHILE(total <= 21)
    {
        # player's turn
        IF(player = 1)
        {
            player = 2
        }
        ELSE
        {
            player = 1
        }
    }
    # game over
}

main()
```

As we can see, we just use a variable that switches between the values $1$ and $2$ to keep track of the current player. At the end of the loop, we have a conditional statement that checks the current value of that variable, and then switches it to the other value. This allows our players to take turns within a single loop.

## Handling Input

Next, we need a way for our players to provide input. Thankfully, earlier in this lab we saw a simple procedure for accepting input from a user and checking to make sure it is valid. So, we can simply borrow that procedure and tweak it a little bit to fit this scenario. Here is what that procedure would look like in pseudocode:

```tex
PROCEDURE read_input(player)
{
    DISPLAY("Enter 1, 2, or 3 for player " + player + ": ")
    x <- INPUT()
    REPEAT WHILE(x != "1" AND x != "2" AND x != "3")
    {
        DISPLAY("Invalid Input!\n")
        DISPLAY("Enter 1, 2, or 3 for player " + player + ": ")
        x <- INPUT()
    }
    RETURN NUMBER(x)
}
```

This procedure is a bit different than the previous one because it requires a parameter. The parameter is used to represent the current player, and we include that in the prompt for input to show which player's turn it is. Without that, the game would be very confusing. We've also updated the Boolean expression inside of the while loop to make sure the value input is either `"1"`, `"2"`, or `"3"`. If it isn't, it will print an error message and prompt the same player for input again. Once a valid input has been received, it will return that value back to where this procedure was called from.

{{% notice note note-1 "Enforcing Whole Numbers" %}}

Unfortunately, in pseudocode, there isn't a good way to require users to input whole numbers. For this example, the number of possible inputs is small enough that it makes the most sense to just check for the individual string values themselves, and then convert the input to a number once it has been verified. There are many other approaches in both pseudocode and Python that will achieve the same result.

{{% /notice %}}

## Completing the Program

Now that we have a procedure for handling input, we must simply add that procedure call to our `main()` procedure, and use it to update the value stored in the `total`. We can also add a message at the end to determine which player is the winner. The final, complete program is shown here:

```tex
PROCEDURE read_input(player)
{
    DISPLAY("Enter 1, 2, or 3 for player " + player + ": ")
    x <- INPUT()
    REPEAT WHILE(x != "1" AND x != "2" AND x != "3")
    {
        DISPLAY("Invalid Input!\n")
        DISPLAY("Enter 1, 2, or 3 for player " + player + ": ")
        x <- INPUT()
    }
    RETURN NUMBER(x)
}

PROCEDURE main()
{
    total <- 0
    player <- 1
    REPEAT WHILE(total <= 21)
    {
        # player's turn
        total <- total + read_input(player)
        IF(player = 1)
        {
            player = 2
        }
        ELSE
        {
            player = 1
        }
    }
    # game over
    DISPLAY("Player " + player + " wins!")
}

main()
```

Notice at the end of the `main()` procedure that we are able to print the player that wins, instead of the losing player. This is because we are switching between players at the end of the while loop, so once the total reaches a value greater than or equal to $21$, we know that we've already switched the `player` variable to be the other player, instead of the one that just caused the game to end. It's a subtle logic choice, but it works well in this case.

Take a moment to work through this program and make sure you understand how it works. We won't do a full code trace, but you are welcome to do so to make sure you are comfortable with it before continuing.

## Testing - Branch & Path Coverage

Now that we've written our program, let's test it to see if it works correctly. Testing this program is a bit different than some of the other programs we've created, mainly because it heavily restricts the inputs that are valid. Each player can only input the strings `"1"`, `"2"`, or `"3"` as valid input. Any other string is invalid, and will result in the loop inside of the `read_input()` procedure repeating.

Therefore, when testing our program, we should make sure we try each of these inputs, but also try some invalid inputs as well. The order the inputs are provided also matters - for path coverage, we want to test the situation where a valid input is provided first and the loop in `read_input()` is skipped, and also the situation where a valid input is provided after an invalid input or two, so the loop in `read_input()` is executed.

Finally, since this program will read inputs many times while it is executing, we can't simply use multiple sets of inputs. Instead, we have to look at entire lists of inputs, where the order that they are provided matters as much as the inputs themselves.

Consider the following list of inputs, which are marked with the player's turn and the updated sum or error:

| Input | Player | Sum/Error |
|:-----:|:------:|:---:|
| `"1"` | 1 | 1 |
| `"2"` | 2 | 3 | 
| `"3"` | 1 | 6 | 
| `"0"` | 2 | error | 
| `"4"` | 2 | error |
| `"1"` | 2 | 7 |
| `"-1"` | 1 | error |
| `"5"` | 1 | error | 
| `"2"` | 1 | 9 |
| `"lizard"` | 2 | error |
| `"(*&#$&*^@"` | 2 | error | 
| `"3"` | 2 | 12 | 
| `"invalid"` | 1 | error |
| `"3"` | 1 | 15 |
| `"broken"` | 2 | error 
| `"2"` | 2 | 17 | 
| `" "` | 1 | error | 
| `"1"` | 1 | 18 |
| `"3"` | 2 | 21 | 
| | | Player 1 Wins |

This list represents one complete game. The first input, `"1"`, will be the first input provided by player 1, then the `"2"` will be player 2's turn, and so on. However, as the inputs progress, we start to see some invalid inputs as well. When the game receives an invalid input, the `read_input()` procedure will enter the loop, and the same player will be prompted for input again until a valid input is received. So, looking through this list, we see that it includes both the situation where the input provided is valid the first time, bypassing the loop, as well as situations where the initial input provided by a player is invalid, entering the loop and prompting for additional input. So, this set of input achieves path coverage in just one game!

We may also want to test and make sure that it is possible for both players to win. To do that, we can simply come up with another set of inputs similar to the one given above, but use different values for the valid inputs to make sure that player 2 wins that game. By doing so, we've achieved every possible outcome of the game.

## Testing - Loop Termination

The other part of testing this program is to show that the loops will terminate properly. You won't be required to prove this yourself in this course, but you should still think about it when designing and testing them. So, let's briefly take a look at that process as well.

First, we can look at the loop in `read_input()` procedure. This is a bit tricky, since the condition for repeating in the loop is entirely driven by user input. So, we really can't say whether the loop will terminate or not, but we can easily show that _if_ the user inputs a valid value, the loop will correctly terminate and the program can continue running. So, as far as our testing goes, that's good enough.

The loop in the `main()` procedure is a bit different. This loop will repeat while the value stored in `total` is less than or equal to $21$. So, to prove this loop will terminate, we need to come up with a **loop variant** and show that it is reducing each time the loop is executed. Thankfully, we can just say that the loop variant is `21 - total`. As the value in `total` increases, that value will decrease until it reaches $0$ or less. 

To show that it is constantly decreasing, we can simply say that the `read_input()` procedure will always return a positive integer, and that value is added to the `total` each time the loop iterates. So, since `total` is always getting larger, the loop variant is getting smaller, and the loop will eventually terminate.

There we go! That's a complete worked example for building and testing a program that contains multiple loops in different procedures. Hopefully this is helpful as you move ahead to the next part of the lab, where you are asked to create and test your own programs. Good luck!
