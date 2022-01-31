---
title: "Complex Python"
pre: "8. "
weight: 80
date: 2021-01-29T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="slides" target="_blank">Slides</a>

Finally, let's look at how we can rewrite some of our previous Python programs by combining expressions into more complex statements. Just like we saw in pseudocode, Python also allows us to perform multiple actions on a single line of code, provided they can all be combined in some way to create a single statement.

Let's consider the example on the previous page, shown here:

```python
def square_sum(one, two):
    one = one * one
    two = two * two
    total = one + two
    return total


def main():
    text_one = input("Enter the first number: ")
    one = int(text_one)
    text_two = input("Enter the second number: ")
    two = int(text_two)
    total = square_sum(one, two)
    print("The sum of squares of {} and {} is {}".format(one, two, total))


main()
```

There are many ways we can write this program to perform the same work. For example, the `square_sum()` function can actually be reduced to a single line of code as seen below:

```python
def square_sum(one, two):
    return (one * one) + (two * two)
```

We can perform multiple mathematical operations in a single expression, and as long as we either use parentheses or pay attention to the order of operations, we'll get the expected answer. We don't have to store the intermediate values in variables, since Python will do that for us when it evaluates the expression.

Likewise, in the `main()` function, we can put the `input()` expression inside of the `int()` function, allowing us to read input as a string and convert it to an integer in a single line:

```python
def main():
    one = int(input("Enter the first number: "))
    two = int(input("Enter the second number: "))
    total = square_sum(one, two)
    print("The sum of squares of {} and {} is {}".format(one, two, total))
```

Finally, we can also move the function call to `square_sum()` directly into the `format()` method in the `print()` statement. When that line is executed, Python will know it has to call the `square_sum()` method first and get the returned value before it can print the output. 

```python
def main():
    one = int(input("Enter the first number: "))
    two = int(input("Enter the second number: "))
    print("The sum of squares of {} and {} is {}".format(one, two, square_sum(one, two)))
```

Of course, if we really wanted to, we could remove the `square_sum()` function entirely, and just compute the value directly in `main()`. However, for this example, we will leave it as a separate function. So, our new program contains this code:

```python
def square_sum(one, two):
    return (one * one) + (two * two)


def main():
    one = int(input("Enter the first number: "))
    two = int(input("Enter the second number: "))
    total = square_sum(one, two)
    print("The sum of squares of {} and {} is {}".format(one, two, total))


main()
```

Functionally, this code will create the exact same output as the previous code, but it will do so using fewer variables and statements. Each statement is simply more complex, consisting of multiple expressions. 

As we discussed in pseudocode, each of these approaches to writing code is valid. They simply follow different coding styles, each one with particular benefits and disadvantages to consider. Sometimes it is better to have more variables and shorter expressions, especially if the overall operation involves many steps and is difficult to follow. Other times it is better to combine a few lines of code together as a single statement to make it very clear what the overall operation is trying to accomplish.

Once again, the best advice is to simply write code in a way that it is readable to you and to anyone else who has to read it. As long as it is clear and performs correctly, it is a good style to follow. As we further develop our skills and gain experience, our style will continue to change over time. 