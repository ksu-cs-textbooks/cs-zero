---
title: "Worked Example"
pre: "4. "
weight: 40
date: 2021-04-23T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Finally, let's go through a complete worked example program that uses dictionaries in Python. Consider the following problem statement:

> Write a program that will compute the score of a given word in a game of [Scrabble](https://en.wikipedia.org/wiki/Scrabble). Assume that there are no special squares present. The program should prompt the user to input a string that only contains letters, and then compute the total score of that string by summing the value assigned to each letter. If the user inputs a string that contains invalid characters, the program should prompt for additional input until a valid word is received.

This is a pretty simple program that can easily make use of a dictionary in Python. So, let's go through the process of solving it!

## Handling Input

As always, we can start our solution by including a `main()` function and a call to the `main()` function at the bottom of our code, as shown here:

```python
def main():


main()
```

Next, we'll probably want to create a function to handle requesting input from the user. So, we'll add that function to our solution as well, and we'll call it from within the `main()` function itself:

```python
def get_input():



def main():
    word = get_input()


main()
```

In the `get_input()` function, we'll need the while loop structure we've already learned to handle input and verify that it is correct, so let's go ahead and add that:

```python
def get_input():
    word = input("Enter a single word: ")
    while # word is not valid
        print("Error! Invalid Input!")
        word = input("Enter a single word: ")
    return word


def main():
    word = get_input()


main()
```

The only part we have to figure out is how we can determine if a word contains only valid characters. There are many different approaches we could follow, but the simplest is to use the `isalpha()` function that is part of the Python `string` data type. This function, along with many others, are described in the [Official Python Documentation](https://docs.python.org/3.6/library/stdtypes.html#text-sequence-type-str). 

So, let's update our code to use that function as the Boolean expression in our while loop:

```python
def get_input():
    word = input("Enter a single word: ")
    while not word.isalpha():
        print("Error! Invalid Input!")
        word = input("Enter a single word: ")
    return word


def main():
    word = get_input()


main()
```

There we go! that covers the `get_input()` function, which will prompt the user to input a string that only contains letters. 

## Computing Score

Next, let's look at writing a function that will accept a single word as a parameter, and then compute the score of that word according to the official Scrabble scoring rules. 

We can start with a simple function definition as shown here:

```python
def compute_score(word):

```

First, let's quickly convert the `word` we are given to lowercase, just in case the user has included any uppercase letters. Remember, we already know that this word should _only_ contain letters, but it may be a mix of uppercase and lowercase. We can use the `lower()` function to make this conversion:

```python
def compute_score(word):
    word = word.lower()

```

Next, we'll need to iterate through each letter in the word. Since we can treat a string just like a list, we can use a for loop for this:

```python
def compute_score(word):
    word = word.lower()
    for letter in word:

```

We'll also need some way to keep track of the total score, and then return that value at the end of the function. This is a pretty common pattern in programming known as the **accumulator pattern**. So, let's add a `total` variable to our program, starting it at $0$ and then returning it at the end:

```python
def compute_score(word):
    word = word.lower()
    total = 0
    for letter in word:
        # add letter's score to total
    return total
```

Finally, we just need some way to convert a letter into a score in Scrabble. Thankfully, we can refer to the [Official Scrabble FAQ](https://scrabble.hasbro.com/en-us/faq) to find out how many points each letter is worth:

* (1 point) - A, E, I, O, U, L, N, S, T, R
* (2 points) - D, G
* (3 points) - B, C, M, P
* (4 points) - F, H, V, W, Y
* (5 points) - K
* (8 points) - J, X
* (10 points) - Q, Z

There are many different ways we could build this program, but one simple way would be to assign each letter a value in a dictionary! To make things even easier, we can leave out all of the letters that are worth 1 point, and just include the letters with higher point values. By doing so, if we don't find our desired letter in the dictionary, we can simply assume that the score must be 1!

So, let's add that dictionary to our code:

```python
def compute_score(word):
    scores = {"d": 2, "g": 2, "b": 3, "c": 3, "m": 3, "p": 3, 
              "f": 4, "h": 4, "v": 4, "w": 4, "y": 4, "k": 5, 
              "j": 8, "x": 8, "q": 10, "z": 10}
    word = word.lower()
    total = 0
    for letter in word:
        # add letter's score to total
    return total
```

Now that we have this dictionary available in our code, we can use it inside of the for loop to compute the total score of the word by looking up the value of each letter. However, before we can directly access a letter, we first must determine if a given letter is contained in the dictionary. In Python, we can do this using the `in` keyword. So, we can add an if statement inside of our for loop that is structured as shown here:

```python
def compute_score(word):
    scores = {"d": 2, "g": 2, "b": 3, "c": 3, "m": 3, "p": 3, 
              "f": 4, "h": 4, "v": 4, "w": 4, "y": 4, "k": 5, 
              "j": 8, "x": 8, "q": 10, "z": 10}
    word = word.lower()
    total = 0
    for letter in word:
        if letter in scores:
            total = total + scores[letter]
        else:
            total = total + 1
    return total
```

The Boolean expression `letter in scores` will return true if the current letter in our word is present as a key in the dictionary scores. The same syntax also works for determining if an element is present in a list!

## Complete Program

We can complete our program by simply printing the score returned by the `compute_score()` function in our `main()` function. So, the complete program is shown below:

```python
def get_input():
    word = input("Enter a single word: ")
    while not word.isalpha():
        print("Error! Invalid Input!")
        word = input("Enter a single word: ")
    return word


def compute_score(word):
    scores = {"d": 2, "g": 2, "b": 3, "c": 3, "m": 3, "p": 3, 
              "f": 4, "h": 4, "v": 4, "w": 4, "y": 4, "k": 5, 
              "j": 8, "x": 8, "q": 10, "z": 10}
    word = word.lower()
    total = 0
    for letter in word:
        if letter in scores:
            total = total + scores[letter]
        else:
            total = total + 1
    return total


def main():
    word = get_input()
    print(compute_score(word))


main()
```

We can confirm our program works correctly by running it and testing a few different inputs, as shown below:

![Output 2](/images/lab14/output2.png)

This example shows a great way to use dictionaries in our program - we can assign values to various keys, and then easily look them up in the dictionary as needed. Feel free to run this example in Python Tutor on your own to see how it works, and see if you can come up with your own high-scoring Scrabble words.