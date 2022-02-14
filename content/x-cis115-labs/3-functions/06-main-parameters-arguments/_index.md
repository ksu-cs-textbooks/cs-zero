---
title: "Main Function, Parameters, & Arguments"
pre: "6. "
weight: 60
date: 2021-01-15T00:00:01-05:00
---

{{< youtube eLcFDbHMIKU >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Let's review a couple other concepts related to functions in Python. These will closely mirror what we've already learned in pseudocode, so we'll cover them pretty quickly here.

## Main Function

Just like in pseudocode, we can also create a **`main` function** in Python. The use of a `main` function in Python is not required at all - Python is designed as a scripting language, meaning we can write code directly in a Python file without using any functions at all. However, it is generally considered good practice to make sure all code is part of a function, and then we can include a `main` function as the starting point for any program.

So, we can update the example we saw previously to include a `main` function by simply placing the three function calls in a new function called `main`, and then including a call to the `main` function at the bottom of the program:

```python
def foo():
    print("eye")


def bar():
    print("to")


def main():
    foo()
    bar()
    foo()


main()
```

From here on out in this course, we'll follow this convention in our complete Python programs. Specifically:

1. All programs must contain a function named `main` as the starting point of the program.
1. All code in a program must be contained within a function, with the exception of a single call to the `main` function at the bottom of the program.

This will make our Python programs easy to follow, and it will help us later on down the road if we choose to learn another language such as Java or C# that requires a main function.

## Function Parameters

Functions in Python can also require **parameters**. To include a parameter in a function, we simply have to include the name of the parameter in the parentheses `()` at the end of the function definition. Multiple parameters should be separated by commas `,`. For example, we can update our `hello_world` function to include a couple of parameters:

```python
def hello_world(first_name, last_name):
    print("Hello ", end="")
    print(first_name, end=" ")
    print(last_name)
```

Here, we are defining two parameters, named `first_name` and `last_name`, that are used as part of the function. Those parameters can be treated just like any other variable within the function. 

## Calling a Function with Arguments

Once we have a function that requires parameters, we can call it by including **arguments** in the parentheses `()` that are part of the function call. For example, we can call the `hello_world` procedure above and provide two arguments like this:

```python
hello_world("Willie", "Wildcat")
```

When we run this code, it will place the string value `"Willie"` in the parameter variable `first_name`, and the string value `"Wildcat"` will be placed in the parameter value `last_name` within the frame for the `hello_world` function. When the code in `hello_world` is executed, we should see the following output:

```tex
Hello Willie Wildcat
```

## Code Tracing a Procedure with Arguments

To see how this works, let's work through a full example. Here's a more complex Python program that includes parameters, arguments, and some other variable expressions:

```python
def flip(first, last):
    temp = first
    first = last
    last = temp
    print(first)
    print(last)


def main():
    first = "Willie"
    last = "Wildcat"
    flip(first, last)
    print(first)
    print(last)


main()
```

Once again, before reading the full analysis below, take a minute to read through this code and see if you can guess what it does. It can be a bit tricky if you don't read it carefully and think about what we've learned so far. 

To trace this example, copy the code into the `tutor.py` file in the `python` folder on Codio, or click this [Python Tutor](https://pythontutor.com/visualize.html#code=def%20flip%28first,%20last%29%3A%0A%20%20%20%20temp%20%3D%20first%0A%20%20%20%20first%20%3D%20last%0A%20%20%20%20last%20%3D%20temp%0A%20%20%20%20print%28first%29%0A%20%20%20%20print%28last%29%0A%0A%0Adef%20main%28%29%3A%0A%20%20%20%20first%20%3D%20%22Willie%22%0A%20%20%20%20last%20%3D%20%22Wildcat%22%0A%20%20%20%20flip%28first,%20last%29%0A%20%20%20%20print%28first%29%0A%20%20%20%20print%28last%29%0A%0A%0Amain%28%29&cumulative=false&heapPrimitives=nevernest&mode=edit&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false) link. 

When we begin, our code trace will look like this example:

![Python Tutor 1](/images/lab3/tutor3_1.png)

As we expect, the first thing that Python will do is scan through the code and record any functions it finds in the global frame. So, after pressing the **Next >** button a couple of times, we should reach this point:

![Python Tutor 3](/images/lab3/tutor3_3.png)

Now we are at a function call for the `main` function. So, when we click the **Next >** button:

![Python Tutor 4](/images/lab3/tutor3_4.png)

Python tutor will jump to that function's code, and it will also create a new frame for variables that are created in the `main` function. The next two lines deal with creating a couple of variables, so we can click the **Next >** button a couple of times to execute those lines and stop when we reach the next function call:

![Python Tutor 7](/images/lab3/tutor3_7.png)

Now we are ready to call the `flip` function. This function requires two parameters, named `first` and `last`. Notice that those parameter names are the **same** names as the variables that we created in the `main` function? This is a common practice in programming - sometimes it is simplest to use the same variable names in multiple functions, especially if they are storing the same data. However, it is important to understand that those variables are not related in any way except for the name, as we'll see in this example. When we click the **Next >** button to jump to the start of the `flip` function, we should see the following in our Python tutor trace:

![Python Tutor 8](/images/lab3/tutor3_8.png)

It has now created a frame for the `flip` function, and copied the values of the two arguments into the appropriate parameter variables. Since we listed the arguments `first` and `last` in that order in the function call to `flip`, a copy of the values from those two variables in `main` will be stored in the same two variable names in `flip`. It's an easy way to make sure the arguments are in the correct order!

The first three lines in the `flip` function will swap the values in the `first` and `last` parameter variables. So, after we've executed those three lines, we should now see this setup in our trace:

![Python Tutor 12](/images/lab3/tutor3_12.png)

Notice that the values in `first` and `last` inside of the `flip` frame have changed, but the values in the same variables in the `main` frame have not changed! This is why it is very useful to keep track of variables in frames within a code trace - we can easily tell which variables go with which function, even if they have the same names. So, the next two lines of code in the `flip` function will simply print out the contents of the `first` and `last` parameter variables:

![Python Tutor 14](/images/lab3/tutor3_14.png)

At this point, we've reached the end of the `flip` function, so when we click the **Next >** button again, we'll jump back down to where we left off in the `main` function. At the same time, we'll remove the `flip` frame from the list of frames, completely removing the `first` and `last` parameter variables used in that function:

![Python Tutor 15](/images/lab3/tutor3_15.png)

Now that we are back in the `main` function, we can see that the values stored in the `first` and `last` variable are unchanged, just like we'd expect. This is important to understand - just because one function uses the same variable names as another function, or that a function's parameter names match the variable names provided as arguments, they are not related and any changes in the function won't impact the values outside of the function. So, we can finish the `main` function by running the last two lines, which will print the current values of `first` and `last` to the screen:

![Python Tutor 17](/images/lab3/tutor3_17.png)

Finally, once the program reaches the end of the `main` function, it will jump back to the `main` function call at the bottom of the program. This will remove the `main` frame from the list of frames. Since there is nothing more to do, the program will end at this point:

![Python Tutor 18](/images/lab3/tutor3_18.png)

The whole process can be seen in this animation:

![Python Tutor Animation 3](/images/lab3/tutor3.gif)

There we go! We've explored how functions, parameters, and arguments all work in Python. Understanding this process now will make it much easier to write complex programs later on. 