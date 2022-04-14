---
title: "Strings are Lists"
pre: "5. "
weight: 50
date: 2021-04-10T00:00:01-05:00
---

{{< youtube KzAfiKbWBTs >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Throughout this course, we've seen several different ways to work with strings. In Python, just like in many other programming languages, it is possible to treat strings as a list of individual characters. Because of this, we can write many useful programs that use and manipulate strings in a variety of ways. 

Let's look at one quick example program that can manipulate strings just like a list! Consider the following Python program:

```python
import random
import string


def encode(secret, step):
    output = ""
    for i in secret:
        output = output + i
        for j in step:
            output = output + random.choice(string.ascii_lowercase)
    return output


def decode(code, step):
    return code[::step]


def main():
    secret = input("Enter a secret word")
    step = int(input("Enter a positive integer"))
    code = encode(secret, step)
    print("Your code is:")
    print(code)
    print()
    decoded = decode(code, step)
    print("I can decode it back to:")
    print(decoded)


main()
```

This is a very simple encoding program that will allow the user to enter a secret phrase, encode it by inserting many random characters between the characters of the word itself, and then show that it can be decoded once again. This is very similar to how a [Scytale](https://en.wikipedia.org/wiki/Scytale) encodes messages.

Let's briefly walk through this example using Python Tutor to see how it works. As always, we can copy and paste this code in the `tutor.py` file in Codio, or click this [Python Tutor](https://pythontutor.com/visualize.html#code=import%20random%0Aimport%20string%0A%0A%0Adef%20encode%28secret,%20step%29%3A%0A%20%20%20%20output%20%3D%20%22%22%0A%20%20%20%20for%20i%20in%20secret%3A%0A%20%20%20%20%20%20%20%20output%20%3D%20output%20%2B%20i%0A%20%20%20%20%20%20%20%20for%20j%20in%20range%28step%20-%201%29%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20output%20%3D%20output%20%2B%20random.choice%28string.ascii_lowercase%29%0A%20%20%20%20return%20output%0A%0A%0Adef%20decode%28code,%20step%29%3A%0A%20%20%20%20return%20code%5B%3A%3Astep%5D%0A%0A%0Adef%20main%28%29%3A%0A%20%20%20%20secret%20%3D%20input%28%22Enter%20a%20secret%20word%3A%20%22%29%0A%20%20%20%20step%20%3D%20int%28input%28%22Enter%20a%20positive%20integer%3A%20%22%29%29%0A%20%20%20%20code%20%3D%20encode%28secret,%20step%29%0A%20%20%20%20print%28%22Your%20code%20is%3A%22%29%0A%20%20%20%20print%28code%29%0A%20%20%20%20print%28%29%0A%20%20%20%20decoded%20%3D%20decode%28code,%20step%29%0A%20%20%20%20print%28%22I%20can%20decode%20it%20back%20to%3A%22%29%0A%20%20%20%20print%28decoded%29%0A%0A%0Amain%28%29&cumulative=false&curInstr=0&heapPrimitives=nevernest&mode=display&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false) link to open it in a browser window.

We can skip ahead to the point where the code enters the main function, as shown in this state:

![Tutor 7](/images/lab13/tutor12_7.png)

Let's assume that the user inputs the string `"password"` for the secret word. That will be stored in the `secret` variable. On the next line, we'll ask the user to input a positive integer:

![Tutor 8](/images/lab13/tutor12_8.png)

For this input, we'll assume the user chooses to input the number $5$. So, we'll store that in the `step` variable in our `main()` function, as shown here:

![Tutor 10](/images/lab13/tutor12_10.png)

At this point, we're ready to call the `encode()` function, which requires two parameters. We'll use the variables `secret` and `step` as the arguments to those parameters, so Python Tutor will create a new frame for the `encode()` function and store those values within it:

![Tutor 12](/images/lab13/tutor12_12.png)

At this point, we can notice one very important difference between strings and lists. Even though a string can be treated like a list, as we'll see in this example program, it is still stored as a single variable item in the frame. So, the `encode()` function's frame now contains a copy of the string `secret`, not a pointer to the original variable in the `main()` function's frame. Technically, we would say that strings are an **immutable** data type, so we cannot change them from within a function like we can do with lists.

Inside of the `encode()` function, we'll start by creating a new variable `output`, which is initially set to store an empty string. 

![Tutor 13](/images/lab13/tutor12_13.png)

Then, we'll reach a for loop. This for loop will iterate through each character in the `secret` string, one at a time. So, just like with a list, each character will be stored in the iterator variable `i` so we can use it inside of our for loop. For the first iteration, we'll store the character `'p'` in the iterator variable `i`, then we'll enter the loop:

![Tutor 14](/images/lab13/tutor12_14.png)

Inside of the loop, the first step is to append the current iterator variable `i` to the `output` string. So, we'll place the character `'p'` at the end of that string:

![Tutor 15](/images/lab13/tutor12_15.png)

Then, we'll reach a second for loop. This loop will repeat `step - 1` times, so we'll enter the loop and set the iterator variable `j` to be $0$ initially.

![Tutor 16](/images/lab13/tutor12_16.png)

Inside of this loop, we have one complex line of code that we haven't seen before. First, we have the `string.ascii_lowercase` list, which is a built-in list that is part of the `string` library which contains all $26$ lowercase letters of the English alphabet. To use this list, we have to include the `import string` line at the top of our file. Then, we use a special function named `random.choice()`, which is used to choose a random element from a list. So, we'll also have to include the `import random` line at the top of our file to use that library as well. Finally, we'll add that character to the end of the `output` string. 

![Tutor 17](/images/lab13/tutor12_17.png)

We'll repeat this process a few more times. Once we exit the innermost for loop, we should be at this state:

![Tutor 24](/images/lab13/tutor12_24.png)

In the `output` variable, we now see the first character of our secret word, `'p'`, followed by four random characters. These random characters make it more difficult for someone to decode our message. We'll repeat this process for each of the other letters in our secret word. So, at the end of the `encode()` function, we should be at this state:

![Tutor 102](/images/lab13/tutor12_102.png)

As we can see, the `output` variable appears to be completely random at first glance, which is exactly what we want. At this point, the `encode()` function will return that string back to the `main()` function, and it will be stored in the `code` variable there.

![Tutor 104](/images/lab13/tutor12_104.png)

Next, the `main()` function will print out some helpful output, and then eventually it will reach the line that calls the `decode()` function. 

![Tutor 107](/images/lab13/tutor12_107.png)

Once again, we'll copy the values in the `code` and `step` variables to the `decode()` function's frame since they are provided as arguments, and then we'll enter the `decode()` function:

![Tutor 109](/images/lab13/tutor12_109.png)

In this function, we see that we can decode our encoded phrase using a simple slicing operation, with the `step` variable providing the key we need to get our secret word out of the encoded string. We'll return that back to the `main()` function:

![Tutor 111](/images/lab13/tutor12_111.png)

There we go! We've shown that we can easily construct an encoded phrase in a string using a secret word and a step variable, and then we can decode that phrase using a simple string slice. At the same time, we were able to explore how strings can be used like lists by iterating through a string and creating slices of a string, but also that strings are **immutable** and aren't passed using **call by reference** like lists are. Instead, strings use **call by value** in Python, so we have to remember to return our updated strings at the end of any functions that manipulate them. 

Thankfully, being able to work with strings in Python using the same methods as lists makes it very easy to write a wide variety of programs that create and manipulate strings!
