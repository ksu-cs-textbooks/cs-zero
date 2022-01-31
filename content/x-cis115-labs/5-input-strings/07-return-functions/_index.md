---
title: "Return in Functions"
pre: "7. "
weight: 70
date: 2021-01-29T00:00:01-05:00
---

{{< youtube ufqVy7lX7Do >}}

#### Resources

* <a href="slides" target="_blank">Slides</a>

Python functions are also capable of returning a value, just like we've seen in pseudocode. In Python, we use the `return` keyword, instead of a `RETURN()` statement, but the concept is the same.

Let's look at a quick example of a full Python program that includes a function that returns a value:

```python
def square_sum(one, two):
    one = one * one
    two = two * two
    total = one + two
    return total


def main():
    text_one = input("Enter the first number: ")
    one = int(text_one)
    text_two = input("Enter the second number: ")
    two = int(text_two)
    total = square_sum(one, two)
    print("The sum of squares of {} and {} is {}".format(one, two, total))


main()
```

To truly understand how this program works, let's use Python Tutor to explore it step by step. Like before, copy the code into the `tutor.py` file in the `python` folder on Codio, or click this [Python Tutor](https://pythontutor.com/visualize.html#code=def%20square_sum%28one,%20two%29%3A%0A%20%20%20%20one%20%3D%20one%20*%20one%0A%20%20%20%20two%20%3D%20two%20*%20two%0A%20%20%20%20total%20%3D%20one%20%2B%20two%0A%20%20%20%20return%20total%0A%0A%0Adef%20main%28%29%3A%0A%20%20%20%20text_one%20%3D%20input%28%22Enter%20the%20first%20number%3A%20%22%29%0A%20%20%20%20one%20%3D%20int%28text_one%29%0A%20%20%20%20text_two%20%3D%20input%28%22Enter%20the%20second%20number%3A%20%22%29%0A%20%20%20%20two%20%3D%20int%28text_two%29%0A%20%20%20%20total%20%3D%20square_sum%28one,%20two%29%0A%20%20%20%20print%28%22The%20sum%20of%20squares%20of%20%7B%7D%20and%20%7B%7D%20is%20%7B%7D%22.format%28one,%20two,%20total%29%29%0A%0A%0Amain%28%29&cumulative=false&curInstr=0&heapPrimitives=nevernest&mode=display&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false) link. 

At the start, our Python Tutor trace will look like this:

![Python Tutor 1](/cc110/images/lab5/tutor4_1.png)

The first few steps are pretty straightforward, since Python will simply move through the code and record all of the functions it finds. Once we reach the call to the `main()` function at the bottom, we'll be at this state:

![Python Tutor 3](/cc110/images/lab5/tutor4_3.png)

So, we'll enter the `main()` function and start executing the code it contains. The first line is an `input()` expression, so Python will prompt the user for input. In Python Tutor, this will open a box at the bottom where we can enter the input, as shown below:

![Python Tutor 5](/cc110/images/lab5/tutor4_5.png)

Let's assume that the user would enter `2` for this input. So, we can type that into the box and press ENTER or click submit. Python tutor will refresh the page to accept the input, and then we'll be at this setup:

![Python Tutor 6](/cc110/images/lab5/tutor4_6.png)

Next, we'll convert the string value `"2"` that is currently stored in the `text_one` variable to an integer using the `int()` function and store it in the variable `one`. On the next line, it will ask for input once again:

![Python Tutor 7](/cc110/images/lab5/tutor4_7.png)

In this case, we'll assume the user is inputting `3`, and then we'll store it and convert it to an integer stored in the variable `two`:

![Python Tutor 9](/cc110/images/lab5/tutor4_9.png)

At this point, we're ready to call the `square_sum()` function. So, Python Tutor will find the arguments for the function call and prepare to store them in the parameter variables of the function. When we click next, we'll see this setup in our window:

![Python Tutor 10](/cc110/images/lab5/tutor4_10.png)

Recall that Python Tutor will create a new frame for the `square_sum()` function in the frames area and store the variables from that function there. This will become important later when we reach the end of the function. Inside of the `square_sum()` function, we just perform a few mathematical operations, culminating with the `total` variable storing the sum of the squares of the two arguments, as shown here:

![Python Tutor 14](/cc110/images/lab5/tutor4_14.png)

At this point, we've reached the `return` statement at the end of the `square_sum()` function. When we click next on Python Tutor, we'll see something new appear:

![Python Tutor 15](/cc110/images/lab5/tutor4_15.png)

When Python reaches the end of a function, it will record the return value in the function's frame before leaving the function. This value is what is given back to the `main()` function. So, when we click next again, we'll see this state:

![Python Tutor 16](/cc110/images/lab5/tutor4_16.png)

We're back in the `main()` function, and now we can see that the new `total` variable stores the value $13$, which was the returned value from the `square_sum()` function. So, on this last line, we'll see that the program will create an output statement using a template string and the string `format()` method, and it will display output to the user:

![Python Tutor 17](/cc110/images/lab5/tutor4_17.png)

What's also interesting to note here is the return value of the `main()` function. Since we didn't include a `return` statement at the end of the function, the return value is set to a special value called `None` in Python. We'll learn about what that value actually represents in a future course. 

The entire process is shown in the animation below:

![Python Tutor 4](/cc110/images/lab5/tutor4.gif)

This review of how a function returns data should be very helpful as we continue to build more complex programs. Remember - we can always paste any Python code into a tool like Python Tutor to run through it step-by-step and see what it really does. 