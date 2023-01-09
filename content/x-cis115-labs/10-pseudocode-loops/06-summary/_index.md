---
title: "Summary"
pre: "6. "
weight: 60
date: 2021-03-16T00:00:01-05:00
---

In this lab, we introduced several major important topics in pseudocode. Let's quickly review them.

## Pseudocode While Loops

While loops in pseudocode will execute while a Boolean expression evaluates to `true`.

```tex
REPEAT WHILE(<boolean expression>)
{
    <block of statements>
}
```

## Pseudocode For Loops

For loops in pseudocode will execute a set number of times.

```tex
REPEAT <n> TIMES
{
    <block of statements>
}
```

## Input with Loops

Loops can be used to request new input from the user if invalid input is received.

```tex
PROCEDURE positive_input()
{
    DISPLAY("Enter a positive number: ")
    x <- NUMBER(INPUT())
    REPEAT WHILE(x <= 0)
    {
        DISPLAY("Invalid Input!\n")
        DISPLAY("Enter a positive number: ")
        x <- NUMBER(INPUT())
    }
    RETURN x
}
```

## Testing Loops

Loops can be tested for both **branch** and **path** coverage. In general, achieving path coverage involves writing code that will enter the loop, and also code that will bypass the loop entirely. 

Loops should also be tested for termination and situations that may result in infinite loops. Using a **loop variant** and showing that it is monotonically decreasing is a helpful technique. 

<!-- TODO Review Fibonacci Problem in Lab? -->