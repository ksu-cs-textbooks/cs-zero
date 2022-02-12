---
title: "Pseudocode Comparators"
pre: "3. "
weight: 30
date: 2021-02-11T00:00:01-05:00
---

{{< youtube >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Another powerful feature of pseudocode are the **comparator** operators, which can be used to create Boolean values by comparing string and number values in an expression. These comparators are a powerful way to build programs that can perform different actions based on data received from the user, as we'll see later in this lab. Let's review the commonly used comparators in pseudocode.

## Equal

The equal comparator `=` is used to determine if two values are equivalent. This operator can be used between any two values, and it will either result in a value of `true` if both values are equivalent, or `false` if they are not. Here are some rules to keep in mind:

1. When comparing strings, the strings must be exactly identical to be equivalent. This means that capitalization, punctuation, and other special symbols must all be exactly the same in both strings.
1. Strings and numbers will never be equivalent, even if the string contains text that would convert to the same numeric value. The same applies to strings and Boolean values. 

For example, we can use the equal comparator to check if two numeric values are equivalent, as shown in this example:

```tex
x <- 5
y <- 3 + 2
DISPLAY(x = y)
```

When executed, this code will display the following output:

```tex
true
```

We can do the same for two strings:

```tex
a <- "Hello " + "World"
b <- "hello " + "world"
DISPLAY(a = b)
```

This time, the output will be:

```tex
false
```

This is because the two string values are not identical - one has capital letters, and the other one does not. 

{{% notice tip tip-1 "Double Equals" %}}

In most other programming languages, the equality comparator is represented by two equals signs `==` instead of a single one `=`. This is because the single equals sign is used in assignment statements in most language, so we use a double equal as the equality comparator to avoid any confusion between the two.

In pseudocode, we use the arrow symbol `<-` for assignment statements, so we can use the single equals sign for equality. However, it is important to remember that this **only** works in pseudocode, and will cause issues if used in other languages such as Python.

{{% /notice %}}

## Not Equal

The next comparator is the not equal comparator, which is typically written as `!=` in pseudocode. Sometimes, we may also see it formatted as the special character `≠`, but we won't use that character in our pseudocode.

The not equal comparator is exactly what it sounds like - it will return `true` if the two values being compared are not equivalent, or `false` if the two values are equivalent. So, the statement `a != b` is the same as saying `NOT (a = b)`. 

Here's an example of using this comparator in pseudocode:

```tex
x <- 5
y <- 5 + 0.000001
DISPLAY(x != y)
```

When executed on our "mental model" of a computer, we should get the following output:

```tex
true
```

This is because the values $5$ and $5.000001$ are not exactly the same value, even though they are very similar. 

## Less Than and Greater Than

The last four comparators are all similar, so we'll cover them all as a group. These comparators are specifically used to compare the relationship between two values, determining an ordering between the two. We should already be familiar with these operators from mathematics:

* `<` less than
* `<=` less than or equal to (sometimes written as `≤` in text)
* `>` greater than
* `>=` greater than or equal to (sometimes written as `≥` in text)

When these comparators are applied to numeric values, they'll compare the two values just like we'd expect from math. For example, we can see these comparators in action in this pseudocode:

```tex
a <- 5
b <- 6
DISPLAY(a < b)
DISPLAY("\n")
DISPLAY(a > b)
```

When we run this code, we'll see the following output:

```tex
true
false
```

These comparators are a bit more confusing when applied to string values. In that case, they will look at the [lexicographic order](https://en.wikipedia.org/wiki/Lexicographic_order) of the two strings, which is similar to alphabetical order but also includes capitalization, punctuation, and other special symbols. We won't cover that in too much detail here, but in most computer programs the letters are sorted according to their order in the [ASCII](https://en.wikipedia.org/wiki/ASCII) encoding standard.

For example, we can compare two strings as shown in this example:

```tex
x <- "test"
y <- "tent"
DISPLAY(x < y)
```

When we run this program in our "mental model" of a computer, we'll see this output:

```tex
false
```

This is because the string `"test"` does not come before `"tent"` when placed in alphabetical order, since `s` comes after `n`. So, we would say that the string stored in `x` is not less than the string stored in `y`, and therefore the result should be `false`.

## Order of Operations

It's also important to note that there are many situations where Boolean operators and mathematical operators are used in the same expression. In those cases, **the mathematical operators are all resolved first**, and then the Boolean operators in this order, going from left to right:

1. Boolean comparators
1. `NOT` operator
1. `AND`
1. `OR`

As always, it is considered good practice to include parentheses in any complex expressions to make sure that the intent is clear, regardless of the order of operations. 

Let's look at a quick example in pseudocode:

```tex
x <- 4 < 5 AND 3 * 5 > 12 OR NOT 7 MOD 3 = 1
```

This expression includes many mathematical operators, as well as Boolean operators and comparators. To evaluate this expression, we must first resolve all mathematical operations first, so we'll evaluate `3 * 5` and `7 MOD 3` and place those results in the expression:

```tex
x <- 4 < 5 AND 15 > 12 OR NOT 1 = 1
```

Next, we'll resolve any comparator operators, moving from left to right. This will convert any remaining numbers into Boolean values. So, we'll evaluate `4 < 5`, `15 > 12`, and `1 = 1` and replace those expressions with the resulting Boolean values:

```tex
x <- true AND true OR NOT true
```

Once we've done that, the next operator to evaluate is the `NOT` operator. So, we'll evaluate `NOT true` to the resulting value `false` and place it back in the expression:

```tex
x <- true AND true OR false
```

Then, we'll handle the `AND` operator, so we'll evaluate `true AND true` to the value `true`:

```tex
x <- true OR false
```

Finally, we'll evaluate the rest of the statement `true OR false` to the value `true`, which will be stored in the variable `x`:

```tex
x <- true
```

As we can see, the order of operations allows us to work through a complex expression like this example. However, in practice, it is always best to include parentheses where needed to make sure the expression is evaluated like we intend it to be.