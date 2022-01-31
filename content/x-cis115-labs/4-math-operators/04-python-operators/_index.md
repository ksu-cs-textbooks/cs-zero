---
title: "Python Operators"
pre: "4. "
weight: 40
date: 2021-01-29T00:00:01-05:00
---

{{< youtube esmWXoTMNY0 >}}

#### Resources

* <a href="slides" target="_blank">Slides</a>

We can also use Python to perform mathematical operations on numerical data using operators. So, let's briefly review the operators we've learned so far, and introduce a couple of new operators that are unique to Python. 

## Mathematical Operators

Python supports the same mathematical operators that we've already seen in pseudocode. The only exception is the the modulo operation is performed using the percent symbol `%` instead of the `MOD` keyword. So, here are the symbols we can use in Python and the operations they perform:

* `+` addition
* `-` subtraction
* `*` multiplication
* `/` division
* `%` modulo

However, there is one major difference between how these operators work in pseudocode and how they work in Python, and it has to do with the fact that Python includes two numerical data types. To deal with this, we have to define how the operators work when applied to different data types.

## Resulting Data Types - Same Type

The basic rule to remember, **if a mathematical operator is applied to two variables of the same data type, the result will also be that data type.**

Let's see what that means in practice. Here's a quick example in Python using the multiplication operator on two integer values:

```python
x = 5
y = 10
z = x * y
print(z)
print(type(z))
```

When we run this code, we should see the following output:

```tex
50
<class 'int'>
```

Since both `x` and `y` are the `int` data type, the result of `x * y` will also be an `int` value, so the variable `z` will have that data type, as shown in this example.

However, there is one exception to this rule, which is the division operator `/`. In Python, the division operator will always return a `float` value, even if it is a whole number. Here's an example that demonstrates that:

```python
a = 9
b = 3
c = 4
x = a / b
print(x)
print(type(x))
print()
y = a / c
print(y)
print(type(y))
```

When we run this program, we'll see the following output:

```tex
3.0
<class 'float'>

2.25
<class 'float'>
```

So, as we can see, even though we are dividing two `int` values, we'll get a `float` value as a result each time we use the division operator.

Following the rule above, if we perform a mathematical operation between two `float` values, the resulting value will always be a `float` as well:

```python
a = 2.5
b = 4.5
c = a + b
print(c)
print(type(c))
```

Running this code will produce this output:

```tex
7.0
<class 'float'>
```

So, even though the result is a whole number, the value that is stored is the `float` data type.

## Resulting Data Types - Different Type

The other rule to remember is **anytime an operation involves a `float` value and an `int` value, the result will be a `float`**. So, if there are mixed types, Python will default to the `float` data type.

This can be seen in the following example:

```python
a = 5
b = 2.0
c = a - b
print(c)
print(type(c))
```

When this code is executed, the output should look like this:

```tex
3.0
<class 'float'>
```

Once again, even though the result is a whole number, because the variable `b` is a `float` value, the entire result will also be a `float` value. 

## New Operators

In Python, we can also introduce two new operators:

* `**` exponentiation (power)
* `//` integer division

First, the double star `**` operator is used to represent the exponentiation operation, sometimes referred to the power operator. In Python, the expression `2 ** 3` would be written mathematically as $2^3$, which is the operation of taking $2$ to the power of $3$, or multiplying $2$ by itself $3$ times. This operator follows the rules listed above for determining what type of data is the result of the operation.

Here's a quick example of using the `**` operator in code:

```python
x = 5 ** 3
print(x)
print(type(x))
```

When this code is run, we see the following output:

```tex
125
<class 'int'>
```

The integer division operator, represented by two forward slashes `//`, is used to perform division that **truncates** the result to an integer. However, it still follows the rules for determining the data type of the result as listed above, so if either of the values in the operation is a `float` value, it will return a `float`, even though the result is an integer.

Let's look at an example with that operator in code:

```python
a = 17.5 // 4.5
print(a)
print(type(a))
```

As we expect, when we run this program, we'll get the following output:

```tex
3.0
<class 'float'>
```

So, we see that this operator will return a `float` value, even though it is truncating the result to an integer, simply because the input values contained a `float`. 

Learning the data types that are returned by a mathematical operator can be tricky, but most programmers slowly develop an intuition of how each operator works and what to expect. So, don't worry too much if this is confusing right now, since it will become much clearer with practice! Also, don't forget that we can always create a simple test program like the examples shown above to confirm the result for any operation.  

## Order of operations

Let's quickly review the order of operations in Python. Thankfully, this is very similar to what we've already seen in pseudocode and in mathematics - we just have to add the two new operators:

1. Operations in parentheses are resolved first, moving from left to right.
1. `**` is resolved second, moving from left to right 
1. `*`, `/`, `//` and `%` are resolved third, moving from left to right.
1. `+` and `-` are resolved fourth, moving from left to right.

Of course, this means that there are now 4 operators that all fit in the "multiplication and division" portion, so we have to carefully make sure they are all taken care of in the correct way. As we learned before it is always best to add extra parentheses to any expression to make the intent very clear instead of relying on the order of operations.