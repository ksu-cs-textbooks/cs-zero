---
title: "For Loops"
pre: "2. "
weight: 20
date: 2021-03-16T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Python also includes a second type of loop that is very useful, the **for loop**. Just like in pseudocode, a for loop is used when we want to repeat the steps a certain number of times. However, in Python, we can't just say that we want to repeat something $10$ times. Instead, we use the built-in `range()` function in Python to generate a list of numbers that we use in our loop. Then, our for loop will repeat once for each number in the list, and we can even access that number using an **iterator variable**

{{% notice note note-1 "Lists in Python" %}}

We'll learn more about lists in Python in a later lab. For now, we're just going to use the `range()` function to generate them for use with for loops.

{{% /notice %}}

## Range Function

The `range()` function can be used in three different ways, depending on the number of arguments given when calling the function:

* `range(stop)` - with a single argument, the `range()` function will generate a list of numbers that begins at $0$ and stops before it reaches the `stop` value. For example, `range(10)` will generate a list of numbers from $0$ through $9$. This is great, since there will be $10$ numbers in total, so a for loop using `range(10)` will repeat $10$ times.
* `range(start, stop)` - with two arguments, the `range()` function will generate a list of numbers that begins at `start` and stops before it reaches the `stop` value. So, `range(3,8)` will generate the list `[3, 4, 5, 6, 7]`. There will be `stop - start` numbers in the range. 
* `range(start, stop, step)` - with three arguments, the `range()` function will generate a list of numbers that begins at `start`, increases by `step` each time, and stops before the `stop` value. Therefore, `range(0, 10, 2)` will generate the list `[0, 2, 4, 6, 8]`. We can also use a negative value for `step` to count backwards. So, `range(5, 0, -1)` will generate the list `[5, 4, 3, 2, 1]`. 

You can read more about the Python `range()` function in the [Python Documentation](https://docs.python.org/3.3/library/stdtypes.html#range)

## For Loops

The general structure of a for loop in Python is shown here:

```python
for <iterator variable> in <list>:
    <block of statements>
```

The first time we reach a for loop, we'll keep track of the `<list>` that we'll be iterating over. In general, once you start repeating in a for loop, the `<list>` cannot be changed. 

If the list contains at least one item, then we'll store the first item in the list in the `<iterator variable>` and enter the for loop to execute the code in the `<block of statements>` When we reach the end of the block, we'll jump back to the top and check to see if the `<list>` contains another item. If so, we'll store that item in the `<iterator variable>` and execute the code in the `<block of statements>` again.

This process will repeat until we've used every item in the `<list>`. Then, we'll jump to the end of the for loop and continue the program from there.

## Code Tracing Example

To really see how a for loop works in Python, let's use Python Tutor to trace through a quick sample program. Consider this Python program:

```python
def main():
    x = int(input("Enter a number: "))
    line = ""
    for i in range(x):
        line = line + "*"
        print(line)


main()
```

Before working through the code in Python Tutor, see if you can determine what this program does just by reading it!

To step through the code, we can load it into Python Tutor by placing it in the `tutor.py` file in the `python` folder on Codio, or clicking this [Python Tutor](https://pythontutor.com/visualize.html#code=def%20main%28%29%3A%0A%20%20%20%20x%20%3D%20int%28input%28%22Enter%20a%20number%3A%20%22%29%29%0A%20%20%20%20line%20%3D%20%22%22%0A%20%20%20%20for%20i%20in%20range%28x%29%3A%0A%20%20%20%20%20%20%20%20line%20%3D%20line%20%2B%20%22*%22%0A%20%20%20%20%20%20%20%20print%28line%29%0A%0A%0Amain%28%29&cumulative=false&curInstr=0&heapPrimitives=nevernest&mode=display&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false) link.

We'll start with the usual default state as shown here:

![Tutor 1](/images/lab11/tutor8_1.png)

The next two steps will find the `main()` function in the code and store it in the global frame, and then it will find the `main()` function call at the bottom of the file. So, once it enters the `main()` function, we should be at this state:

![Tutor 3](/images/lab11/tutor8_3.png)

The next line will read the input from the user. For this example, let's assume the user inputs the string `"5"`:

![Tutor 4](/images/lab11/tutor8_4.png)

This means that we'll store the number $5$ in the variable `x`. The program will also create an empty string value in the `line` variable, which we'll use to generate output. At that point, we should have reached the beginning of the for loop.

![Tutor 6](/images/lab11/tutor8_6.png)

Behind the scenes, Python will generate a list of numbers based on the `range()` function. Since the `range()` function is called with a single argument, we know it will be a list of numbers starting at $0$ and ending before it reaches the value in `x`, which is $5$. So, the list will contain the numbers `[0, 1, 2, 3, 4]`, and it will cause the for loop to repeat $5$ times. For the first iteration of the loop, Python will store the first number in the list, $0$, in the iterator variable `i`. In programming, we typically use the variable name `i` to represent our iterator variable. So, once the program has entered the loop, we should see this state:

![Tutor 7](/images/lab11/tutor8_7.png)

Inside of the loop, the first statement will update the `line` value by adding an asterisk `*` to the end of the string. So, after this statement is executed, the `line` variable will store a string containing a single asterisk.

![Tutor 8](/images/lab11/tutor8_8.png)

The second statement will print the `line` variable to the output.

![Tutor 9](/images/lab11/tutor8_9.png)

At this point, we've reached the end of the for loop, so our execution pointer jumps back up to the top of the loop. Then, we check to see if the list we are iterating through contains more values. Again, this list isn't shown in Python tutor, so we have to mentally keep track, but we can see the current value in `i`, and we know what the list contains by looking at the `range()` function. So, we'll update `i` to store the value $1$, and repeat the loop once again.

![Tutor 10](/images/lab11/tutor8_10.png)

Just like before, this iteration will add an asterisk to the string in the `line` variable, and then print that to the output before repeating once again.

![Tutor 12](/images/lab11/tutor8_12.png)

There are still more items in the list, so we'll update `i` to the value $2$ and enter the loop:

![Tutor 13](/images/lab11/tutor8_13.png)

In the loop, we'll update `line` to contain one more asterisk, and then print it before looping back to the top.

![Tutor 15](/images/lab11/tutor8_15.png)

The list still isn't empty, so we'll update `i` to be $3$ this time:

![Tutor 16](/images/lab11/tutor8_16.png)

And then we'll update `line` and print it.

![Tutor 18](/images/lab11/tutor8_18.png)

By now, we should have a pretty good idea of what this loop does. There's one more item in the list, so we'll update `i` to be $4$:

![Tutor 19](/images/lab11/tutor8_19.png)

Inside the loop, we'll add one more asterisk to `line` and then print it.

![Tutor 21](/images/lab11/tutor8_21.png)

Finally, we're back at the top of the loop. Since there are no more items left in the list, we can jump to the bottom of the for loop and continue the program from there. In this case, there's no more code left in the `main()` function, so it will end and the program will terminate. 

Looking at the output, we see that this program will print a right triangle of asterisks that is `x` lines tall and `x` characters wide at the bottom.

A full execution of this program is shown in this animation.

![Tutor 8 Animated](/images/lab11/tutor8.gif)

As we can see, working with for loops in Python is a quick and easy way to repeat a block of statements a specific number of times using the `range()` function.

## Converting to a While Loop

It is possible to convert any for loop using the `range()` function in Python to a while loop. This can be done following a simple three-step pattern:

1. Set an initial value for the iterator variable before the loop
1. Update the iterator value at the end of each loop iteration
1. Convert to a while loop and check the ending value of the iterator variable in the Boolean expression

Let's look at the `main()` function from the example above:

```python
def main():
    x = int(input("Enter a number: "))
    line = ""
    for i in range(x):
        line = line + "*"
        print(line)
```

To convert this for loop into a while loop, we can follow the three steps listed above. First, we must set an initial value for our iterator variable `i` before the loop. Since the first value stored in `i` is $0$, we'll set it to that value.

```python
def main():
    x = int(input("Enter a number: "))
    line = ""
    i = 0
    for i in range(x):
        line = line + "*"
        print(line)
```

Next, we need to update the value of the iterator variable at the end of each loop iteration. Since we didn't provide an argument for the `step` value in the `range()` function, we know that `i` will just be incremented by $1$ each time. So, we'll add a short line to increment `i` at the bottom of the loop:

```python
def main():
    x = int(input("Enter a number: "))
    line = ""
    i = 0
    for i in range(x):
        line = line + "*"
        print(line)
        i = i + 1
```

Finally, we can switch the for loop to a while loop. In the Boolean expression, we want to repeat the loop while the iterator variable `i` has not reached the maximum value. So, we'll use the Boolean expression `i < 5` in the new while loop:

```python
def main():
    x = int(input("Enter a number: "))
    line = ""
    i = 0
    while i < 5:
        line = line + "*"
        print(line)
        i = i + 1
```

There we go! That's the basic process for converting any for loop using `range()` in Python to be a while loop. It's a useful pattern to know and recognize when it is used in code.
