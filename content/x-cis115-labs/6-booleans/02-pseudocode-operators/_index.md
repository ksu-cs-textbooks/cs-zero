---
title: "Pseudocode Operators"
pre: "2. "
weight: 20
date: 2021-02-11T00:00:01-05:00
---

{{< youtube SWwj46lGAkI >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

There are also many special operators that can be used to perform operations on Boolean values. These operators are used to along with one or more Boolean values in some way to produce a resulting value. Let's review the three important Boolean operators in pseudocode.

## AND Operator

The first Boolean operator we'll review is the `AND` operator. This operator is used to determine if both Boolean values are `true`, and if so the resulting value will also be `true`. Otherwise, it will be false. This corresponds to the following truth table:

| Variable 1 | Variable 2 | Result |
|:----------:|:----------:|:------:|
| F | F | F |
| F | T | F |
| T | F | F |
| T | T | T |

Here's an example of using the `AND` operator in pseudocode:

```tex
x <- true
y <- true
z <- x AND y
DISPLAY(z)
```

When this code is executed, the following output should be displayed:

```tex
true
```

## OR Operator

The next Boolean operator to review in pseudocode is the `OR` operator. This operator will result in a `true` value if at least one of the input values is `true`. If both inputs are `false`, then the result is `false`. This corresponds to the following truth table:

| Variable 1 | Variable 2 | Result |
|:----------:|:----------:|:------:|
| F | F | F |
| F | T | T |
| T | F | T |
| T | T | T |

Here's an example of using the `OR` operator in pseudocode:

```tex
a <- true
b <- false
c <- a OR b
DISPLAY(c)
```

When this code is executed, the following output should be displayed:

```tex
true
```

## NOT Operator

Finally, the other Boolean operator we'll learn about is the `NOT` operator. This operator is only applied to a single Boolean value, and it is used to negate the value. This means that an input value of `true` will result in `false`, and vice-versa. This corresponds to the following truth table:

| Variable 1 | Result |
|:----------:|:------:|
| F | T |
| T | F |

Here's an example of using the `NOT` operator in pseudocode:

```tex
x <- true
y <- NOT x
DISPLAY(y)
```
Once again, when this code is executed, we'll see the following output:

```tex
false
```

These three operators allow us to perform the basic Boolean logic operations needed to build more complex programs. 
