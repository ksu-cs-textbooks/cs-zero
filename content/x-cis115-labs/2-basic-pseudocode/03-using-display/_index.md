---
title: "Using Display"
pre: "3. "
weight: 30
date: 2021-01-07T00:00:01-05:00
---

{{< youtube 9iGLfxxCNSw >}}

#### Resources

* <a href="slides" target="_blank">Slides</a>

Now that we've been introduced to the `DISPLAY(expression)` statement, let's write a few simple programs using that statement to see how it works. Again, we're just learning how to run these programs using our "mental model" of a computer, so it is really important for us to closely pay attention to both the code and the output of these examples. We have to learn what rules govern how our computer should work, and the only way to do that is to explore lots of different programs and see what they do.

## Example 1 - Multiple Statements

First, let's write a simple program that prints 4 letters separated by spaces:

```tex
DISPLAY("a b c d")
```

Just like our "Hello World" program, when we run this program, we'll see that string printed in the user interface:

```tex
a b c d
```

Ok, that makes sense based on what we've previously seen. The `DISPLAY(expression)` statement will simply display any string expression in our user interface.

Of course, programs can consist of multiple statements or lines of code. So, what if we write a program that contains multiple `DISPLAY(expression)` statements, like this one:

```tex
DISPLAY("one")
DISPLAY("two")
DISPLAY("three")
DISPLAY("four")
```

What do you think will happen when we try to execute this program on our "mental model?" Have we learned a rule that tells us what should happen yet? Recall on the previous page we learned that it will print the value on the user interface, but that's it. So, when we execute this program, we'll see the following output:

```tex
onetwothreefour
```

That's a very interesting result! We might expect that four lines of code would produce four lines of output, but in fact they are all printed on the same line! This is very helpful, since we can use this to construct more complex sentences of output by using multiple `DISPLAY(expression)` statements. 

If we want to add spaces between each line, we'll need to include that in our expressions somehow. For example, we could rewrite the program like this:

```tex
DISPLAY("one ")
DISPLAY("two ")
DISPLAY("three ")
DISPLAY("four")
```

Notice that there is now a space inside of the quotation marks on the first three statements? That will result in this output:

```tex
one two three four
```

There are many other ways we could accomplish this, but this is probably the simplest to learn.

## Example 2 - Multiple Lines

What if we want to print output on multiple lines? How can we do that? In this case, we need to introduce a special symbol, the **newline** symbol. In our pseudocode, as in most programming languages, the newline symbol is represented by a backslash followed by the letter "n", like `\n`, in a string. When our user interface sees a newline symbol, it will move to the next line before printing the rest of the string. The newline symbol itself won't appear in our output.

For example, we can update our previous program to contain newline symbols between each letter:

```tex
DISPLAY("a\nb\nc\nd")
```

This might be a bit difficult to read at first, but as we become more and more familiar with reading code, we'll start to see special symbols like the newline symbol just like any other letter. For now, we'll just have to read closely and make sure we are on the lookout for special symbols in our text.

When we run this program in our "mental model" of a computer, we should see the following output on our user interface:

```tex
a
b
c
d
```

There we go! We've now figured out how to print text on multiple lines.

## Example 3 - Multiple Statements on Multiple Lines

We can even extend this to multiple statements! For example, we can update another one of our previous programs to print each statement on a new line by simply adding a newline character to the end of each string:

```tex
DISPLAY("one\n")
DISPLAY("two\n")
DISPLAY("three\n")
DISPLAY("four")
```

When we execute this program, we'll get the following output:

```tex
one
two
three
four
```

That's pretty much all we need to know in order to use the `DISPLAY(expression)` statement to do all sorts of things in our programs!

{{% notice note note-1 "Differences in Official AP CSP Pseudocode" %}}

In this course, we have already introduced one big difference between the AP CSP Pseudocode and our own pseudocode language. In the [official CSP Exam Reference Sheet](https://apcentral.collegeboard.org/pdf/ap-computer-science-principles-exam-reference-sheet.pdf), the `DISPLAY(expression)` statement is explained as follows:

> Displays the value of `expression`, followed by a space.

By that definition, each use of the `DISPLAY(expression)` statement will add a space to the output. So, programs like this:

```tex
DISPLAY("one")
DISPLAY("two")
```

will produce nice, clean output like this:

```tex
one two
```

We believe this is done to simplify the formatting for answers on the AP exams, which must be hand-written. By automatically including the space in the `DISPLAY(expression)` statement, it becomes easy to construct a single line of output consisting of multiple parts, and they will be spaced nicely.

However, when trying to print output on multiple lines, the AP CSP Pseudocode does not provide a clear definition for how to accomplish that. For example, adding a newline symbol at the end of the line, like this:

```tex
DISPLAY("one\n")
DISPLAY("two")
```

will result in output with an awkward space at the beginning of the second line:

```tex
one
 two
```

This _could_ be resolved by adding the newline at the beginning of the next line, like so:

```tex
DISPLAY("one")
DISPLAY("\ntwo")
```

However, this is **rarely** done in real programming languages, since most languages have a display statement that adds a newline at the end by default, and most programmers are used to that convention. Therefore, we don't feel that it is proper to teach this method, only to adjust later on to fit with a more proper style. 

Likewise, there is no way to use a `DISPLAY(expression)` statement without adding a space at the end, which is something that is very useful in many situations.

Therefore, we've chosen to redefine the `DISPLAY(expression)` statement to **not** append a space at the end of the line. That aligns it with statements that are available in most common programming languages. 

{{% /notice %}}