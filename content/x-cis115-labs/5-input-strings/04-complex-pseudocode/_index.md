---
title: "Complex Pseudocode"
pre: "4. "
weight: 40
date: 2021-01-29T00:00:01-05:00
---

{{< youtube 47MaR6OYakw >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Previously, we worked through this simple example pseudocode program:

```tex
DISPLAY("Enter a number: ")
text <- INPUT()
number <- NUMBER(text)
square <- number * number
DISPLAY("The square of your input is ")
DISPLAY(square)
```

However, we can greatly shorten this program's code using a couple of programming features that we have not covered yet. Let's look at how we can do that.

## Expressions of Expressions

The single biggest thing to understand about expressions in programming is that we can usually combine them in a variety of different ways.

For example, this program receives input from the user using the `INPUT()` expression, and then on a separate line of code it uses the `NUMBER()` procedure to convert it to a number and store it in a variable. However, since the `NUMBER()` procedure allows us to use any expression as an argument, we can combine those two lines:

```tex
DISPLAY("Enter a number: ")
number <- NUMBER(INPUT())
square <- number * number
DISPLAY("The square of your input is ")
DISPLAY(square)
```

Yup, that's right! Because `INPUT()` is essentially a procedure that returns a value, we can directly use that returned value as an argument to the `NUMBER()` procedure, without ever storing it in a variable. Our "mental model" of a computer will call the procedure inside the parentheses first, just like we'd expect, and then once it returns a value it will use that value to call the other procedure.

We can combine the last two lines of code in a similar way. We've already seen how to combine strings using the concatenation operator, so as long as we convert the value in `square` to a string it will work:

```tex
DISPLAY("Enter a number: ")
number <- NUMBER(INPUT())
square <- number * number
DISPLAY("The square of your input is " + STRING(square))
```

So, we'll just place the `square` variable in the `STRING()` procedure to convert it to a string value, and then we can concatenate that value onto the end of the other string and display it in a single line.

Finally, we can even perform operations directly inside of procedure calls. So, we can combine the last two lines in this new example, preventing us from even needing the `square` variable at all:

```tex
DISPLAY("Enter a number: ")
number <- NUMBER(INPUT())
DISPLAY("The square of your input is " + STRING(number * number))
```

Our computer knows to resolve any expressions used as an argument in a procedure before calling the procedure, so this will work exactly like we'd expect it to. So, we've taken a program with 6 lines of code and reduced it to just 3 lines of code, and removed 2 of the 3 variables it uses in the process. 

## Concise and Readable

The real question is: which of these two examples is best? That is, which one is the preferred coding style to learn? The answer is that it really depends - both have their merits, and functionally they will work nearly identically on most modern computers and programming languages.

It really is a question of style - is it better to have more lines of code and variables, clearly spelling out what each step of the process is, or is it better to have shorter programs with more complex lines of code but maybe fewer variables? For beginning programmers, it is usually recommended to follow the first style, using as many variables as needed and focusing on short, concise lines of code over large, complex statements. 

However, as we become more accustomed to programming, we'll find that many times it is easier to read and understand complex statements, and our code can be written in a way that better reflects what it is actually doing. 

This is very similar to learning how to read, write, and speak in a new language. We must start with short, concise sentences, and slowly build up our knowledge of more complex statements and grammar rules until we become a fluent speaker. 

Overall, the best advice to follow is to make your code readable to both yourself and anyone else who may have to read and maintain the code. As long as it is clear what the code is doing based on what it says, it is probably a good style to follow. As we continue to learn more, we'll slowly refine our coding style to be one that is easy to follow and understand for everyone. 