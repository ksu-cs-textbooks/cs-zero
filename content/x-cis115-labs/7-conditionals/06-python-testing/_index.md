---
title: "Python Testing"
pre: "6. "
weight: 60
date: 2021-02-11T00:00:01-05:00
---

{{< youtube >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Previously, we saw how important it was to consider many possible test inputs when testing a program that contains a conditional statement. Let's go through one more example, this time in Python, to get some more practice with creating test inputs for conditional statements.

## Example Program

For this example, let's consider the following program in Python:

```python
def main():
    a = int(input("Enter a number: "))
    b = int(input("Enter a number: "))
    if a // b >= 5:
        # Branch 1
        print("{} goes into {} at least 5 times".format(b, a))
    else:
        # Branch 2
        print("{} is less than 5 times {}".format(a, b))
    if a % b == 0:
        # Branch 3
        print("{} evenly divides {}".format(b, a))
    else:
        # Branch 4
        print("{} / {} has a remainder".format(a, b))


main()
```

This program is a bit trickier to evaluate. First, it accepts two numbers as input. Then, it will check to see if the first number is at least 5 times the second number. It will print an appropriate message in either case. Then, it will check to see if the first number is evenly divided by the second number, and once again it will print a message in either case.

## Branch Coverage

To achieve **branch coverage**, we need to come up with a set of inputs that will cause each print statement to be executed. Thankfully, the branches are numbered using comments in the Python code, so it is easy to keep track of them.

Let's start with an easy input - we'll set `a` to $25$ and `b` to $5$. This means that `a // b` is equal to $5$, so we'll go into branch 1 in the first if statement. The second if statement will go into branch 3, since `a % b` is exactly $0$ because $5$ stored in `b` will evenly divide the $25$ stored in `a` without any remainder. So, we've covered branches 1 and 3 with this input.

For another input, we can choose $21$ for `a` and $5$ for `b`. In the first if statement, we'll see that `a // b` is now $4$, so we'll go into branch 2 instead. Likewise, in the second if statement we'll execute branch 4, since `a % b` is equal to $1$ with these inputs. That means we've covered branches 2 and 4 with these inputs.

Therefore, we can achieve branch coverage with just two inputs:

* $25$ and $5$
* $21$ and $5$

## Path Coverage

Recall that there are four paths through a program that consists of two if statements in a row:

1. Branch 1 -> Branch 3
2. Branch 1 -> Branch 4
3. Branch 2 -> Branch 3
4. Branch 2 -> Branch 4

We've already covered the first and last of these paths, so we must simply find inputs for the other two.

One input we can try is $31$ and $5$. In the first if statement, we'll go to branch 1 since `a // b` will be $6$ this time. However, when we get to the second if statement, we'll find that there is a remainder of $1$ after computing `a % b`, so we'll go to branch 4 instead. This covers the second path.

The third path can be covered by inputs $20$ and $5$. In the first if statement, we'll go to branch 2 because `a // b` is now $4$, but we'll end up in branch 3 in the second if statement since `a % b` is exactly 0.

Therefore, we can achieve path coverage with these four inputs:

* $25$ and $5$
* $21$ and $5$
* $31$ and $5$
* $20$ and $5$

## Edge Cases

What about edge cases? For the first if statement, we see the statement `a // b >= 5`, so that clues us into the fact that we'll probably want to try values that result in the numbers $4$, $5$, and $6$ for this statement. Thankfully, if we look at the inputs we've already tried, we can see that this is already covered! By being a bit deliberate with the inputs we've been choosing, we can not only achieve branch and path coverage, but we can also choose values that test the edge cases for various Boolean expressions as well.

Likewise, the Boolean statement in the second if statement is `a % b == 0`, so we'll want to try situations where `a % b` is exactly $0$, and when it is some other value. Once again, we've already covered both of these instances in our sample inputs!

So, with a bit of thinking ahead, we can come up with a set of just 4 inputs that not only achieve full path and branch coverage, but also properly test the various edge cases that are present in the program!