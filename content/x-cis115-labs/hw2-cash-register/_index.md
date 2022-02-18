+++
title = "Cash Register"
date = 2022-02-18T00:23:05-05:00
hidden = true
pre = "<b>HW 2. </b>"
+++

## Implementing a Cash Register

In the second programming assignment, we're going to build a simple cash register to help us manage simple transactions, calculate tax, and make change. Each of these processes is a great way to practice using conditional statements and boolean logic in our code.

{{% notice note note-1 "Learning Objectives" %}}

The goal of this assignment is to demonstrate understanding of the following topics in Python:

* Boolean Logic
* Conditional Statements
* Mathematical Operators
* Functions, Parameters, Arguments, and Return

{{% /notice %}}

### Tax-Exempt Status

Many organizations also enjoy tax-exempt status, meaning they do not have to pay any sales tax on the items they purchase. Usually this is reserved for non-profit entities or governmental groups. Our program will first ask the user if they are tax exempt, and if so our program will not charge any sales tax at all. In that case, we'll simply ask the user to input a single value:

* The total amount of goods purchased

We can use that value in the rest of our program.

### Taxable vs. Non-Taxable Goods

For users who are not tax-exempt, we must compute a subtotal that includes sales tax. In many areas, certain goods are taxed at different rates. For example, in many states, most food items are not subject to sales tax at all. So, in this program, we're going to model that by asking the user to input two values:

* The total amount of taxable goods purchased
* The total amount of non-taxable goods purchased

These two values will be used to compute the total amount purchased by the user.

### Computing the Subtotal

Once the user has confirmed whether they are tax-exempt or not, and entered the various totals, our program will compute their subtotal. For users with tax-exempt status, this is simple - the subtotal is simply the amount of goods purchased that the user input.

If the user is not tax-exempt, then the total amount will be computed by this formula:

$$
\text{taxable} * 1.125 + \text{non-taxable} = \text{total}
$$

We will be using the tax rate $12.5\%$ in this program. Since we are adding that to the total of taxable goods, we just multiply that value by $1.125$, since this is the same value as $\text{taxable} + \text{taxable} * 0.125$.

### Making Change

Once we've determined the total amount for the user, we will also ask the user to input a cash amount they wish to pay. That amount must be equal to or greater than the amount owed - otherwise the program should simply print an error.

If the user pays more than what is owed, we'll need to make change. So, we can subtract the two amounts to find the change that is owed, and then we need to determine what bills and coins must be given to the user. 

For this program, we'll use the American monetary system with the following bills and coins available:

* \\\$$1.00$ bill
* \\\$$0.25$ quarter coin
* \\\$$0.05$ nickel coin
* \\\$$0.01$ penny coin

**While there are other denominations we could use, we're limiting ourselves to just these 4 to simplify the program.**

The process for making change in a computer program is _different_ than the process that most of us have learned for computing change by hand. For most of us, we learned to start with the total amount that the user is being charged, and then add the smallest denomination (the penny) until we reach a multiple of $5$, then add nickels and dimes to get to the next quarter, then add quarters to get to the next whole dollar, and so on, until we reach the amount that the user paid. This process works well mentally, but is difficult to program.

Instead, our program should work in the other direction. We start by computing the amount of change to be given, and then determine how many of the largest denomination fit into that amount. We can do this using the truncated division operator `//` when working with whole dollar amounts. Likewise, we can use the modulo operator `%` to determine how much change is left to be given. 

We can repeat this process for the other denominations. However, because they are not whole numbers, the truncated division operator `//` does not work. To solve this, **we can multiply the amount of change to be given by $100$ first, and then convert that value to an `int` value.** In effect, we'll be working with a whole number of pennies instead of dollars and cents.

### Making Change Example

Let's work through a brief example. Let's assume that the user is owed \\\$$2.94$ in change. So, our first step is to multiply that value by $100$ and convert it to an `int`:

$$
2.94 * 100 = 294
$$

This tells us that we owe the user the equivalent of $294$ pennies. Now, we start with the largest denomination, and determine how many of those fit into the given value. Since we've multiplied everything by $100$, we know that a dollar bill is actually worth $100$ pennies. So, we'll find the result of dividing $294$ by $100$ using truncated division:

$$
294 \text{ // } 100 = 2
$$

So, we owe the user $2$ dollar bills. To find the remaining amount of change to give, we'll use the modulo operator:

$$
294 \text{ % } 100 = 94
$$

We still have $94$ cents to give. The next denomination is the quarter, which is worth $25$ cents. So, we can repeat the same process:

$$
94 \text{ // } 25 = 3
$$
$$
94 \text{ % } 25 = 19
$$

That means we owe the user $3$ quarters, with $19$ cents left over. We do this again for the nickels, which will also give us the number of pennies:

$$
19 \text{ // } 5 = 3
$$
$$
19 \text{ % } 5 = 4
$$

So, in total, we owe the user $2$ dollars, $3$ quarters, $3$ nickels, and $4$ pennies, for a total of \\\$$2.94$

## The Assignment

Write your program in a file named `homework2.py` inside the `python` folder in Codio. This should be a **complete Python program** consisting of the following elements:

1. A `get_totals()` function
1. A `make_change(amount)` function
1. A `main()` function
1. A call to the `main()` function

Each function will be described in detail below.

## The Get Totals Function

The `get_totals()` function should not require any parameters. When the function is called, it should first prompt the user to input whether they are tax-exempt or not:

* If the user inputs either the string `"yes"` or `"true"`, they are considered tax-exempt.
* If the user inputs any other value, they are not tax-exempt.

If the user is determined to be tax-exempt, simply prompt the user to input a total amount of goods purchased as a decimal number. If the user is not tax-exempt, prompt the user to input both the amount of taxable goods purchased as well as the amount of non-taxable goods purchased, both as decimal numbers.

Once the user has input all required values, this method should compute the total as described above and print output in the following format:

```tex
Your total today is ${subtotal}
```

Finally, the function should **return** the total back to the `main()` function.

{{% notice info info-1 "Formatting Dollar Amounts" %}}

Notice that each dollar amount is formatted using commas if needed, as well as only two digits after the decimal place. Recall that you can do this by using the placeholder `${:,.2f}` in Python, as in this example:

```python
print("Your total today is ${:,.2f}".format(12.3456))
```

which will print:

```tex
You have $12.35 in your account
```

You can refer to the [Python Documentation](https://docs.python.org/3/library/string.html#formatstrings) for more information these format specifications.

{{% /notice %}}

## The Make Change Function

The `make_change()` function requires **a single parameter**, the total amount owed by the user (the return value from the `get_totals()` function above). This function should prompt the user to input an amount to pay as a decimal number. 

If the amount to pay is strictly less than the total amount owed, this function should simply print `"Error! Not enough money paid"` and end the function. 

If the amount to pay is equal to the total amount owed, this function should simply print `"No change needed"` and end the function.

Otherwise, this method should compute the change to be given following the method described above, and produce output in the following format:

```tex
You are owed ${change} in change:
{a} dollars {b} quarters {c} nickels {d} pennies.
```

However, if any of the values `a`, `b`, `c`, or `d` in the output above are $0$, that denomination should be omitted from the output. For example, if the user is only owed $2$ quarters and $3$ pennies, the output should be:

```tex
You are owed $0.53 in change:
2 quarters 3 pennies.
```

The `make_change()` function **does not** return a value.

{{% notice info info-2 "Ending a Function Early" %}}

In Python, any function can be ended early by simply including a `return` statement in the code, as in this example:

```python
if <boolean expression>:
    print("Error!")
    return
```

We **should not** use `sys.exit()` to end a Python program from within a function, even though many online resources refer to this method. Alternatively, we can place the rest of the code for the function in the `else:` branch of the conditional statement:

```python
if <boolean expression:
    print("Error")
    return
else:
    <remaining code>
```

{{% /notice %}}

{{% notice tip tip-1 "Floating-Point Precision Errors" %}}

There is a slight chance that you'll run into issues with floating-point precision errors, where your results are off by one penny in either direction. This is due to the imprecise nature of floating-point numbers. Dealing with that appropriately is outside the scope of this class. You will not be penalized if your program encounters one of these errors while it is being graded.

{{% /notice %}}

## The Main Function

The `main()` function should first call the `get_totals()` function, and then use the returned value from that function to call the `make_change()` function. That is all that the `main()` function should do - all other code must be in either the `get_totals()` or the `make_change()` functions.

## Documentation & Comments

You may add any comments to your code to help explain how it works. In Python, you can use the hash symbol `#` (also known as a pound sign or octothorpe) in front of a line of text in a Python file to make it a comment:

```python
# This is a code comment
x = 15
y = 7  # comments can be at the end of lines, too
```

Your file should also include a **documentation comment**, also known as a **docstring** at the top of your file. The **docstring** should be formatted like this:

```python
"""
File Name: <filename>
Author: <your name>
Version: <submission date>
Section: <your section>
Description: <detailed description of this program>
"""
```

Notice that the start and end of the documentation comment uses three double-quotes `"""` on a single line.

## Sample Execution

Below are a couple of screenshots showing a sample execution of the model solution for this homework assignment. Your submission should have similar functionality and output, but the text for input prompts may differ slightly:

![Sample Run 1](/images/hw2/hw2a.png)

![Sample Run 2](/images/hw2/hw2b.png)

## Submitting

Once you have completed this program, upload your `homework2.py` file to the assignment on Canvas. 