---
title: "Dictionaries and Functions"
pre: "3. "
weight: 30
date: 2021-04-23T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Finally, let's briefly look at how dictionaries operate when used as parameters to functions in Python. As we can probably guess from the earlier example in Python Tutor, dictionaries also use **call by reference**, just like lists.

Here's a short example program in Python that demonstrates the use of dictionaries with functions.

```python
def add_score(scores):
    name = input("Enter a name: ")
    score = int(input("Enter a score: "))
    scores[name] = score


def average_score(scores):
    total = 0
    for key, value in scores.items():
        total = total + value
    return total / len(scores)


def main():
    scores = {}
    for i in range(4):
        add_score(scores)
    print(average_score(scores))


main()
```

Let's take a look at this program using Python Tutor to see how it works. As always, you can copy and paste this code into the `tutor.py` file on Codio, or click this [Python Tutor](https://pythontutor.com/visualize.html#code=def%20add_score%28scores%29%3A%0A%20%20%20%20name%20%3D%20input%28%22Enter%20a%20name%3A%20%22%29%0A%20%20%20%20score%20%3D%20int%28input%28%22Enter%20a%20score%3A%20%22%29%29%0A%20%20%20%20scores%5Bname%5D%20%3D%20score%0A%0A%0Adef%20average_score%28scores%29%3A%0A%20%20%20%20total%20%3D%200%0A%20%20%20%20for%20key,%20value%20in%20scores.items%28%29%3A%0A%20%20%20%20%20%20%20%20total%20%3D%20total%20%2B%20value%0A%20%20%20%20return%20total%20/%20len%28scores%29%0A%0A%0Adef%20main%28%29%3A%0A%20%20%20%20scores%20%3D%20%7B%7D%0A%20%20%20%20for%20i%20in%20range%284%29%3A%0A%20%20%20%20%20%20%20%20add_score%28scores%29%0A%20%20%20%20print%28average_score%28scores%29%29%0A%0A%0Amain%28%29&cumulative=false&curInstr=0&heapPrimitives=nevernest&mode=display&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false) link in the lab to open it in a web browser.

First, Python Tutor will iterate through the code and record all of the functions in the objects area. Once it reaches the call to the `main()` function at the bottom, it will jump to the code inside of that function. At that point, we should see this state:

![Tutor 6](/images/lab14/tutor14_6.png)

The first thing that this program will do is create an empty dictionary in the `scores` variable. So, after executing that line of code, we'll see a new dictionary in the objects area in memory as shown here:

![Tutor 7](/images/lab14/tutor14_7.png)

Next, we'll reach a simple for loop that will iterate $4$ times, so we'll enter that loop:

![Tutor 8](/images/lab14/tutor14_8.png)

Inside of the loop, we are calling the `add_score()` function and providing the `scores` dictionary as an argument. So, when Python Tutor jumps to execute that function's code, we'll see it create a new frame for the function and populate that frame with the arguments provided as part of the function call:

![Tutor 9](/images/lab14/tutor14_9.png)

Since dictionaries in Python also use **call by reference**, we'll see that the `scores` parameter in the `add_score()` function's frame is just a reference back to the same empty dictionary that was created earlier. The `scores` variable in the `main()` function's frame also points to the same object in memory. 

The `add_scores()` function will prompt the user to input a name and a score. So, if we assume that the user inputs the string `"Name"` as the name, and `"95"` as the score, we should see this state in Python Tutor:

![Tutor 12](/images/lab14/tutor14_12.png)

The last line of the function will add a new key-value pair to the dictionary, with the name used as the key and the score as the value. So, when the function is ready to return, we should see this state:

![Tutor 13](/images/lab14/tutor14_13.png)

At this point, the control flow will return back to the main function, so our frame for the `add_score()` function will be removed. Thankfully, we can see that the new item we added to the dictionary is present in the one dictionary object in memory, which is also referenced from the `main()` function's frame. So, once we are back in the `main()` function, we'll see this state:

![Tutor 14](/images/lab14/tutor14_14.png)

As we can see, dictionaries properly follow **call by reference**, so if we modify a dictionary that is passed to a function as an argument, we don't have to return it back if we are just working with the same object.

At this point, the program will repeat that process three more times. We'll skip ahead a bit to the end of the for loop in the main function, which will be this state:

![Tutor 36](/images/lab14/tutor14_36.png)

Here, our program will call the `average_score()` function to get the average of all of the scores in the dictionary. So, we'll jump up to that function and provide the current dictionary as an argument, as shown here:

![Tutor 37](/images/lab14/tutor14_37.png)

This function is very straightforward. However, let's skip ahead a bit to when we are inside of the for loop, just to see what that looks like:

![Tutor 40](/images/lab14/tutor14_40.png)

In our code, we are using the `items()` function of the dictionary to allow us to iterate over a list of the key-value pairs in the dictionary. So, inside of that for loop, we see both a `key` and a `value` variable, and they are populated with the first key and value from within our dictionary. 

Once we've iterated through the entire dictionary, we'll be at this state:

![Tutor 49](/images/lab14/tutor14_49.png)

We're ready to return from the function, and we've computed that our return value will be $92.5$, as seen the frame for the `average_score()` function. Once we are back in the `main()` function, we'll simply print that value to the output:

![Tutor 50](/images/lab14/tutor14_50.png)

As we've seen in this example, working with dictionaries and functions in Python is practically identical to what we saw with lists - both data structures use **call by reference** when they are passed as arguments to a function. So, as long as we understand how Python is storing the data in memory, we can effectively build programs that operate the way we expect them to.
