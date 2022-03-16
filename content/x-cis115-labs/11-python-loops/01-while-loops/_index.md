---
title: "While Loops"
pre: "1. "
weight: 10
date: 2021-03-16T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

The first type of loop to explore in Python is the **while loop**. A while loop uses a Boolean expression, and will repeat the code inside of the loop as long as the Boolean expression evaluates to `True`. These loops are typically used when we want to repeat some steps, but we aren't sure exactly how many times it must be done. Instead, we typically know that there is some condition that must be `True` while we repeat the code, and once it turns `False` we can stop looping and continue with the program.

The general syntax for a while loop in Python is shown here:

```python
while <boolean expression>:
    <block of statements>
```

Notice that this syntax is very similar to an if statement. We start with the keyword `while`, followed by some sort of a `<boolean expression>` that will evaluate to either `True` or `False`. The Boolean expression in Python does not need to be placed inside of parentheses, unlike in pseudocode. After the Boolean expression is a single colon `:`. Then, starting on the next line and indented one level is a `<block of statements>` that will be executed when the Boolean expression evaluates to `True`. Once again, just like in an if statement, we know which statements are part of the block within a while loop based solely on indentation. 

Just like in pseudocode, it is possible for the Boolean expression to evaluate to `False` initially, which will bypass the loop entirely and never execute the code inside of it. Likewise, if we aren't careful, we can also write a loop where the Boolean expression will always be `True`, and the loop will run infinitely, causing our program to lock up and never terminate. 

## Code Tracing Example

To truly understand how a while loop works in Python, let's go through a simple code tracing example in Python Tutor. Consider the following Python program:

```python
def main():
    x = int(input("Enter a number from 0 to 100: "))
    total = 0
    while total % 100 != x:
        total = total + 9
    print("The smallest multiple of 9 that ends in {} is {}".format(x, total))


main()
```

See if you can figure out what this program does before moving on!

As always, you can copy and paste this code in the `tutor.py` file in Codio, or click this [Python Tutor](https://pythontutor.com/visualize.html#code=def%20main%28%29%3A%0A%20%20%20%20x%20%3D%20int%28input%28%22Enter%20a%20number%20from%200%20to%20100%22%29%29%0A%20%20%20%20total%20%3D%200%0A%20%20%20%20while%20total%20%25%20100%20!%3D%20x%3A%0A%20%20%20%20%20%20%20%20total%20%3D%20total%20%2B%209%0A%20%20%20%20print%28%22The%20smallest%20multiple%20of%209%20that%20ends%20in%20%7B%7D%20is%20%7B%7D%22.format%28x,%20total%29%29%0A%0A%0Amain%28%29&cumulative=false&curInstr=0&heapPrimitives=nevernest&mode=display&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false) link.

When we load this code in Python Tutor, we should see the usual default state:

![Tutor 1](/images/lab11/tutor7_1.png)

The first couple of steps will simply find the `main()` method and record it in the global frame, and then call the `main()` method from the bottom of the program

![Tutor 3](/images/lab11/tutor7_3.png)

The first line of the program will prompt the user for input and store it in the variable `x`. For this example, let's assume the user inputs the string `"27"`.

![Tutor 4](/images/lab11/tutor7_4.png)

Therefore, we'll store the value $27$ in the variable `x`. The next line will store the value $0$ in the variable `total`, as shown here:

![Tutor 6](/images/lab11/tutor7_6.png)

At this point, we've reached the beginning of the while loop. So, we'll need to determine if the Boolean expression evaluates to `True` or `False`. In this case, the value of `total % 100` is equal to $0$, so it is not equal to the value stored in `x`. Therefore, the Boolean expression is `True`, and we should enter the loop.

![Tutor 7](/images/lab11/tutor7_7.png)

Inside of the loop, we are simply adding $9$ to the value in `total`. So, we'll see that variable is updated, and the execution pointer goes back to the top of the loop. 

![Tutor 8](/images/lab11/tutor7_8.png) 

Now that we are back at the top of the loop, we need to check the Boolean expression again. This time the value of `total % 100` is $9$, which still isn't equal to the value stored in `x`, so we'll enter the loop again.

![Tutor 9](/images/lab11/tutor7_9.png) 

We'll add $9$ to the `total` here, and jump to the top again.

![Tutor 10](/images/lab11/tutor7_10.png) 

Once again, we will check the Boolean expression and see that it is still `True, so we'll enter the loop and add $9$ to the `total` yet again before repeating the process from the top of the loop. At this point, we should see this state in Python tutor.

![Tutor 12](/images/lab11/tutor7_12.png) 

When we compute `total % 100`, we get the value $27$, which is the same as the value stored in `x`. This will make the Boolean expression evaluate to `False`, so we can skip the loop and jump to the bottom of the program.

![Tutor 13](/images/lab11/tutor7_13.png) 

Here, we are simply printing out the output, and then the program will terminate.

![Tutor 14](/images/lab11/tutor7_14.png) 

A full animation of this program's execution in Python Tutor is shown here.

![Tutor Animation 7](/images/lab11/tutor7.gif)

Tracing the execution of a while loop is quite simple, especially with tools such as Python Tutor to help us make sure we're updating the variables in the correct order. 