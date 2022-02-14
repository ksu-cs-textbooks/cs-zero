---
title: "Python Input"
pre: "5. "
weight: 50
date: 2021-01-29T00:00:01-05:00
---

{{< youtube 1-1wbLIYNy4 >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

The Python programs we've written up to this point are very static - each time we run the program, it will perform the same exact operations. Since we're running these programs on a real computer, it might be helpful to build programs that can read and respond to input from the user, making them much more useful overall. Python includes many different ways to handle user input, but in this lab we'll just focus on the simple `input()` function.

## Input in Python

The `input()` function is used to display a prompt the user and then record input. It works very similarly to the `INPUT()` expression we've already seen in pseudocode, but in Python we can display the prompt to the user directly in the `input()` function itself.

Let's look at a quick example:

```python
name = input("Enter your name: ")
print("Hello ", end="")
print(name)
```

Here, we see that the `input()` function actually accepts a message as an argument, which will be displayed to the user. After the message is printed, the user will be given a cursor to enter text immediately after it. Once the user presses the ENTER key, the `input()` function will read the input that was entered and store it as a string value or `str` data type in the `name` variable. 

For example, if the user inputs `Willie Wildcat` at the prompt, this program's output will look like this:

```tex
Enter your name: Willie Wildcat
Hello Willie Wildcat
```

We can see this even more clearly in the terminal. When we first run the program, we'll see the prompt `"Enter your name:"` printed, followed by a cursor prompting the user to enter something:

![Terminal Before Input](/images/lab5/terminal1.png)

Once the user types the input and presses ENTER, the rest of the program will run:

![Terminal Before Input](/images/lab5/terminal2.png)

Now we see the cursor is at the next command prompt, ready to run another program.

## Numerical Input

Of course, we can also read numerical input in Python using the `input()` function. To do this, we must simply use either the `int()` or `float()` function to convert the input received as a string to the correct data type.

Here's a quick example program that requires two inputs for the price and quantity of an item being purchased:

```python
text_one = input("Enter the price of one item: ")
price = float(text_one)
text_two = input("Enter the quantity of items: ")
quantity = int(text_two)
cost = price * quantity
print("The total cost is $", end="")
print(cost)
```

If the user wishes to purchase $3$ items at the price of $2.75$ per item, then the program's output would look like this:

```tex
Enter the price of one item: 2.75
Enter the quantity of items: 3
The total cost is $8.25
```

In the program, we simply read each input from the user as a string value, then use the appropriate conversion function to convert it to the correct data type. For numbers including a decimal point, we use `float()`, but for whole numbers we use the `int()` function.

This works well if the user enters values that make sense. But, what if the user wishes to purchase a fraction of an item? Will this program work? Unfortunately, if the user enters a value with a decimal point for the second input, it can no longer be converted to an integer and we'll get an error:

```tex
Enter the price of one item: 2.75
Enter the quantity of items: 3.5
Traceback (most recent call last):
  File "tutor.py", line 4, in <module>
    quantity = int(text_two)
ValueError: invalid literal for int() with base 10: '3.5'
```

For right now, there's not much we can do about that error other than write programs that clearly tell the user what type of data is expected, but later we'll learn how to handle errors like this and prompt the user for input again.

