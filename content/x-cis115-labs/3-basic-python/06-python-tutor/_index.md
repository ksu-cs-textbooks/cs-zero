---
title: "Code Tracing with Python Tutor"
pre: "6. "
weight: 60
date: 2021-01-15T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="slides" target="_blank">Slides</a>

As we learn to write more complex programs in Python, it is important to make sure we can still mentally execute the code we are writing in our "mental model" of a computer before we actually run it on a computer. After all, if we don't have at least an idea of what the code actually does before we write it, we really haven't learned much about programming!

Thankfully, when working in a real programming language such as Python, there are many tools to help us visualize how the code works when we run it. This helps us continue to develop our "mental model" of a computer by looking behind the scenes a bit to see what is happening when we run our code. 

One such tool is [Python Tutor](https://pythontutor.com/), a website that can quickly run short pieces of Python code to help us visualize what each line does and how it works. This tool is also integrated directly into Codio!

## Python Tutor Example

Let's look at an example of how Python Tutor compares to the manual code traces we performed in a previous lab. For this example, we're going to use the following code:

```python
x = "Hello"
y = x
print(y, end=" ")
x = "World"
print(x, end=", ")
print(y)
```

In Codio, we can see the visualization in a tab to the left. It will visualize the content in the `tutor.py` file in the `python` directory, so make sure that the contents of the `tutor.py` file match the example above before continuing.

Outside of Codio, this visualization can be found by clicking this [Python Tutor Link](https://pythontutor.com/visualize.html#code=x%20%3D%20%22Hello%22%0Ay%20%3D%20x%0Aprint%28y,%20end%3D%22%20%22%29%0Ax%20%3D%20%22World%22%0Aprint%28x,%20end%3D%22,%20%22%29%0Aprint%28y%29&cumulative=false&heapPrimitives=nevernest&mode=edit&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false) to open Python Tutor on the web.

## Stepping Through Code

The initial setup for Python Tutor is shown in the image below:

![Python Tutor 1](/cc110/images/lab3/tutor1.png)

This looks similar to the setup we used when performing code tracing with pseudocode. We have an arrow next to our code that is keeping track of the next line to be executed, and we have areas to the side to record variables and outputs. In Python Tutor, the variables are stored in the **Frames** section. We'll learn why that is important later in this lab when we start looking at Python functions. 

So, let's click the **Next >** button once to execute the first line of code. After we do that, we should see the following setup in Python Tutor:

![Python Tutor 2](/cc110/images/lab3/tutor2.png)

That line is an **assignment statement**, so Pyhton Tutor added an entry in the **Frames** section for the variable `x`, showing that it now contains the string value `"Hello"`. It placed that variable in a frame it is calling the "Global frame," which simply contains variables that are created outside of a function in Python.

When we click the **Next >** button again, we should see this:

![Python Tutor 3](/cc110/images/lab3/tutor3.png)

Once again, the line that was just executed is an assignment statement, so Python Tutor will add a new variable entry for `y` to the list of variables. It will also store the string value `"Hello"`. Just like before, notice that the variable `y` is storing the same value as `x`, but it is a _copy_ of that value. The variables are not connected in any other way. 

We can click **Next >** again to execute the next line of code:

![Python Tutor 4](/cc110/images/lab3/tutor4.png)

Once this line is executed, we'll see that it prints the value of the variable `y` to the output. Python Tutor will look up the value of `y` in the **Frames** section and print it in the output, but it won't evaluate the expression in the code like we did when we performed code tracing in pseudocode. It's a subtle difference, but it is worth noting.

Once again, we can click **Next >** to execute the next assingment statement:

![Python Tutor 5](/cc110/images/lab3/tutor5.png)

This statement will update the value stored in the variable `x` to be the string value `"World"`. After that, we can run the next statement:

![Python Tutor 6](/cc110/images/lab3/tutor6.png)

That statement prints the value of `x` to the output, followed by a comma `,` and a space as shown in the `end` argument provided to the `print` function. Finally, we can click **Next >** one more time to execute the last line of code:

![Python Tutor 7](/cc110/images/lab3/tutor7.png)

This will print the value of `y` to the output. Once the entire program has been executed, we should see the output `Hello World, Hello` printed to the screen.

The full process is shown in the animation below:

![Python Tutor](/cc110/images/lab3/tutor.gif)

Using tools like Python Tutor to step through small pieces of code and understand how the computer interprets them is a very helpful way to make sure our "mental model" of a computer accurately reflects what is going on behind the scenes when we run a piece of Python code on a real computer. So, as we continue to show and discuss examples in this course, feel free to use tools such as Python Tutor, as well as just running the code yourself, as a great way to make sure you understand what the code is actually doing.