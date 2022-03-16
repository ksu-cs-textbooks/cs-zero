---
title: "Input with Loops"
pre: "3. "
weight: 30
date: 2021-03-16T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Loops in Python are also a great way to handle situations where a user must input a value that meets certain criteria. Previously, we used an if statement to determine if the input was valid, but if it wasn't valid all we could do was print an error and end the program. If we use a loop instead, we can prompt the user to provide additional input until we receive a valid value.

To make this process easy to use, we can develop a function just to handle input from the user. For example, if we want the user to input a percentage, we could use a function similar to this one:

```python
def input_percentage():
    x = float(input("Enter a percentage as a decimal number from 0 to 1: "))
    while(x < 0 or x > 1):
        print("Invalid Input!")
        x = float(input("Enter a percentage as a decimal number from 0 to 1: "))
    return x
```

This function starts by prompting the user to input a number, and stores it as a floating-point value in the variable `x`. Then, it will reach the start of the while loop. The Boolean expression will check to see if the value provided is not a percentage, so if it is less than $0$ or greater than $1$ it is considered invalid. 

If the input is invalid, we'll print an error and prompt the user for input again. We'll keep repeating this process until the user provides a value between $0$ and $1$, at which point the loop will terminate. The last line in the function will return that value back to where it was called from.

## Reading Input

With a function such as that in our program, we can use it in another function such as the `main()` function to actually read input directly from the user. For example, we can write a quick program to calculate a weighted average of exam scores as shown below:

```python
def input_percentage():
    x = float(input("Enter a percentage as a decimal number from 0 to 1: "))
    while(x < 0 or x > 1):
        print("Invalid Input!")
1.         x = float(input("Enter a percentage as a decimal number from 0 to 1: "))
    return x


def main():
    print("This program will compute weighted average for three exam scores")
    print("Enter the first exam's score")
    exam1_score = input_percentage()
    print("Enter the first exam's weight")
    exam1_weight = input_percentage()
    print("Enter the second exam's score")
    exam2_score = input_percentage()
    print("Enter the second exam's weight")
    exam2_weight = input_percentage()
    print("Enter the third exam's score")
    exam3_score = input_percentage()
    print("Enter the third exam's weight")
    exam3_weight = input_percentage()
    total = exam1_score * exam1_weight + exam2_score * exam2_weight + exam3_score * exam3_weight
    print("Your total score is {}".format(total))


main()
```

A quick execution of this program is shown here:

![Execution of Program](/images/lab11/input.png)

Take a minute to confirm that the program works by running it yourself, either in Python Tutor or directly in Python. You can even adapt this program to help calculate your final grade in this course!

Learning to how to create building blocks of larger programs, such as the `input_percentage()` function described here, is a great way to develop our programming skills. If we can learn to take a large program and break it down into smaller, repeatable chunks, then the entire program becomes much easier to develop and maintain.
