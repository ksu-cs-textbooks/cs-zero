---
title: "Pseudocode Operators"
pre: "2. "
weight: 20
date: 2021-01-29T00:00:01-05:00
---

{{< youtube I_Mpenj2ZyQ >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Now that we have the ability to store numerical data in variables in pseudocode, we should also learn how to manipulate that data into something new. To do that, let's learn about **operators**. An **operator** in programming is a special symbol that can be used in an expression to manipulate the data in some way. Most operators are **binary operators**, which means they perform an operation that uses two values as input and produces a single value as output. In fact, in some programming languages, the operators themselves are implemented as procedures in the language!

An expression containing a binary operator typically follows this format:

```tex
<expression> <operator> <expression>
```

As before, the `<expression>` parts can be any valid expression in the language, and the `<operator>` part is typically a single symbol, but it can also be a short keyword as well.

Thankfully, these operators should all be very familiar to us from mathematics already, so this is just a quick discussion of how they can be used in programming.

## Addition and Subtraction

For starters, we can use the plus `+` and minus `-` symbols as operators to perform addition and subtraction in pseudocode, just like in math. For example, we can add two variables together to create a third variable as shown in this example:

```tex
a <- 5
b <- 7
c <- a + b
DISPLAY(c)
```

When we run this code on our "mental model" of a computer, we should get this result:

```tex
12
```

Likewise, we can subtract two variables using the minus symbol `-` as shown here:

```tex
x <- 24
y <- 10
z <- x - y
DISPLAY(z)
```

This code should produce this output:

```tex
14
```

## Multiplication and Division

In pseudocode, we use the asterisk `*`, sometimes referred to as the star symbol, to multiply two values together. For example, we can find the product of two values as shown in this pseudocode block:

```tex
a <- 6
b <- 7
c <- a * b
DISPLAY(c)
```

When we run this code, we should see the following result displayed to the user:

```tex
42
```

Division is performed using the slash `/` symbol. A great way to think of division in programming is just like a fraction, since it uses the same symbol between the two numbers. For example, if we execute this code:

```tex
x <- 27
y <- 3
z <- x / y
DISPLAY(z)
```

we would see this output:

```tex
9
```

What if the division would result in a remainder? In that case, we'll simply use decimal values in pseudocode so that the result is exactly correct. For example, if we try to divide $19$ by $5$, as in this example:

```tex
a <- 19
b <- 5
c <- a / b
DISPLAY(c)
```

Our "mental model" of a computer would produce the following output:

```tex
3.8
```

So, as we can see, all of these operators in pseudocode work exactly like their counterparts in math. Even though we aren't running our code on an actual computer, we should be easily able to use a simple calculator to help us perform these operations if needed.

## Modulo Operator

There is one other operator that is used commonly in pseudocode - the **modulo operator**. The **modulo operator** is used to find the **remainder** of a division operation. If we think back to math again, we've probably learned how to perform [long division](https://en.wikipedia.org/wiki/Long_division) when dividing two values. At the end, we might be left with a remainder, or a portion of the first number that is left over after the operation is complete. In many computer programs, that value is very useful, so we have a special operator we can use to find that value. In pseudocode, we use the keyword `MOD` as the modulo operator.

For example, if we want to find the remainder after dividing $19$ by $5$, we would use the following code:

```tex
x <- 19
y <- 5
z <- x MOD y
DISPLAY(z)
```

When we run this code, we would get the following output:

```tex
4
```

This is because the value $5$ will fit into the value $19$ only $3$ times, and then we'll have the value $4$ left over. Mathematically, we are saying that $19 / 5 = (3 * 5) + 4$. Since $4$ is the leftover portion, it is the resulting value when we use the modulo operator. 

In this course, we'll only worry about how the modulo operator works when applied to positive whole numbers. In practice, it can be applied to any numerical value, including decimal values and negative numbers, but those values are not really useful in most cases. So, to keep things simple, we'll only use positive whole numbers with this operator.

## Order of Operations

Finally, just like in mathematics, we must also be aware of the order that these operators are applied, especially if they are combined into a single expression. Thankfully, the same rules we learned in mathematics apply in programming as well. Specifically, operators in pseudocode are applied in this order:

1. Operations in parentheses are resolved first, moving from left to right.
1. `*`, `/` and `MOD` are resolved second, moving from left to right.
1. `+` and `-` are resolved third, moving from left to right.

In most cases, it is best to include parentheses whenever we include multiple operators on the same line, just so the intended interpretation is perfectly clear. However, let's work through a quick example just to see the order of operations in practice.

Here's a complex expression in pseudocode that we can try to evaluate:

```tex
x <- 8 / 4 + 5 * (3 + 1) - 7 MOD 4
```

Looking at our order of operations, the first step is to handle any expressions inside of parentheses. So, we'll first start with the expression `(3 + 1)` and evaluate it to `4`.

```tex
x <- 8 / 4 + 5 * 4 - 7 MOD 4
```

Then, we'll go right to left and perform any multiplication, division, and modulo operations. This means we'll evaluate `8 / 4`, `5 * 4` and `7 MOD 4` and replace them with the resulting values:

```tex
x <- 2 + 20 - 3
```

Finally, we'll perform addition and subtraction from left to right. So, we'll evaluate `2 + 20` first, and then subtract `3` from the result of that operation. At the end, we'll have this statement:

```tex
x <- 19
```

So, we were able to use our knowledge of the order of operations to evaluate that complex expression to a single value, $19$, which will be stored in the variable `x`. 