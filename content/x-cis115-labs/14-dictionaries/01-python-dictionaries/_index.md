---
title: "Python Dictionaries"
pre: "1. "
weight: 10
date: 2021-04-23T00:00:01-05:00
---

{{< youtube OCFZhReWBIw >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

In theory, a **dictionary** is very similar to a list in Python - it is a data structure that can store many different items within a single variable. However, instead of just storing single values as elements and assigning them sequential indexes, dictionaries store a number of **key-value pairs**. A **key** is any value that can be used as a unique identifier for the associated **value** to be stored in the dictionary.

For example, we can use a dictionary to store the "score" for various words in the game of [Scrabble](https://en.wikipedia.org/wiki/Scrabble). In this case, our key would be the word stored as a string, such as `"test"`, and the value would be an integer representing the score, `4`. These two items make up a key-value pair `("test", 4)` that can be stored in a dictionary.

There is one major rule that dictionaries must follow - each key in a dictionary must be unique. Or, put another way, if the dictionary already contains a value for a given key, and we try to add another value that uses the same key, the first value will be overwritten. So, we must be careful and make sure that the keys we choose to use are indeed unique so that they will work in a dictionary.

## Creating a Dictionary

Dictionaries in Python can be created in much the same way as a list. We can create an empty dictionary using a set of curly braces `{}` as shown here:

```python
dict_1 = {}
```

We can also create a dictionary that contains some initial key-value pairs by placing them inside of the curly braces. Each key-value pair is separated by a comma `,` with the key provided first, followed by a colon `:` and then the value. Here's a brief example:

```python
dict_2 = {"a": 1, "b": 2, "c": 3}
```

In this dictionary, the keys are the strings `"a"`, `"b"`, `"c"`, and each one is associated with the values `1`, `2`, and `3`, respectively. 

Finally, to make it a bit easier to read our code, we can also reformat the code to create a dictionary across multiple lines, with each key-value pair shown on its own line as seen in this example:

```python
dict_3 = {
    "cat": "mammal",
    "lizard": "reptile",
    "goldfish": "fish",
    "chickadee": "bird"
}
```

This dictionary associates various animal species with the common name of their classification within the animal kingdom. 

## Adding Items to a Dictionary

We can also easily add new items to a dictionary by simply providing a key inside of square brackets `[]` and then using an assignment statement to assign that key a value. Consider this example:

```python
dict_1 = {}
dict_1["Kansas"] = "Topeka"
dict_1["Nebraska"] = "Lincoln"
dict_1["Missouri"] = "Jefferson City"
```

Here, we start by creating an empty dictionary, and then we can add key-value pairs using the names of states as the key and the state's capital city as the value. 

{{% notice note note-1 "Square Brackets" %}}

Notice that we use square brackets `[]` to access individual items in a dictionary, just like with lists, but we use curly braces `{}` to create a dictionary. This can cause confusion for many new Python programmers. So, pay special attention to the syntax of each data structure, and remember that it can sometimes be difficult to tell whether a data structure in Python is a list or a dictionary without reading the code to see where it was created. 

{{% /notice %}}

## Accessing Items in a Dictionary

Once a dictionary contains items, we can access the value associated with a given key by providing that key within square brackets `[]` after the variable storing the dictionary. Here's an example of what that looks like in Python:

```python
dict_3 = {
    "cat": "mammal",
    "lizard": "reptile",
    "goldfish": "fish",
    "chickadee": "bird"
}

print(dict_3["cat"])   # mammal
```

As we can see, we're able to provide the key `"cat"` and then access the associated value `"mammal"` that was stored in the dictionary.

What if we try to access a key that doesn't exist? In that case, Python will raise a "KeyError" and the program will crash. So, we'll have to be careful and make sure we only try to access keys that are actually stored in the dictionary, unless we are using them in an assignment statement to add a new key-value pair. 

## Updating Items

We can also update the value associated with a given key in a dictionary using an assignment statement, as shown here:

```python
dict_3 = {
    "cat": "mammal",
    "lizard": "reptile",
    "goldfish": "fish",
    "chickadee": "bird"
}

dict_3["cat"] = "feline"

print(dict_3["cat"])   # feline
```

In this example, we are simply replacing the value for the key `"cat"` with a new string "feline". Remember that the keys in a dictionary must be unique, so if we try to add a new value using the same key, it will simply overwrite the existing value associated with that key.

## Dictionaries in Python Tutor

To really understand how dictionaries work in Python, let's go through a quick example using Python Tutor. Consider the following Python program:

```python
def main():
    base = int(input("Enter a whole number: "))
    powers = {}
    for i in range(6):
        powers["{}^{}".format(base, i)] = base ** i
    print(powers)


main()
```

This program will ask the user to provide a number as input, and then it will populate a dictionary where the key is a string representing a mathematical expression including that number, and the value will be the result of that expression. Let's trace through this program in Python Tutor. As always, you can copy and paste the code in the `tutor.py` file in Codio, or click this [Python Tutor](https://pythontutor.com/visualize.html#code=def%20main%28%29%3A%0A%20%20%20%20base%20%3D%20int%28input%28%22Enter%20a%20whole%20number%3A%20%22%29%29%0A%20%20%20%20powers%20%3D%20%7B%7D%0A%20%20%20%20for%20i%20in%20range%286%29%3A%0A%20%20%20%20%20%20%20%20powers%5B%22%7B%7D%5E%7B%7D%22.format%28base,%20i%29%5D%20%3D%20base%20**%20i%0A%20%20%20%20print%28powers%29%0A%0A%0Amain%28%29&cumulative=false&curInstr=20&heapPrimitives=nevernest&mode=display&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%223%22%5D&textReferences=false) link to open it on the web.

When we start tracing the program in Python Tutor, we can skip ahead until it reaches the first line of code in the `main()` function, at which point we'll see this state:

![Tutor 4](/images/lab14/tutor13_4.png)

This first line of code asks the user to input a value. For this example, let's assume the user inputs the string `"3"`. So, we'll store the integer value $3$ in the `base` variable as seen here:

![Tutor 5](/images/lab14/tutor13_5.png)

This line will create an empty dictionary in the `powers` variable. Just like lists in Python, a dictionary is actually stored in the objects area in memory, and the variable is simply a pointer, or reference, to the location in memory where the dictionary will be stored. So, after we execute that line of code, we should see this state:

![Tutor 6](/images/lab14/tutor13_6.png)

At this point, we reach the for loop. This loop will iterate $6$ times, so we'll start by storing the first value $0$ in the iterator variable `i` and then entering the loop:

![Tutor 7](/images/lab14/tutor13_7.png) 

Inside of the loop, we see a single line of code that is pretty complex. This line will actually perform three different operations! First, it will generate a string using the string `format()` method, which will become the new key that is added to the dictionary. Then, it will compute the value of the `base` variable raised to the power of `i`. Finally, it will store that computed value in the dictionary associated with the newly created key. Once all of those steps are complete, we'll see a new item in the dictionary as shown here:

![Tutor 8](/images/lab14/tutor13_8.png) 

In Python Tutor, we can see the key for the item on the left, and then the associated value on the right. So, it is similar to how a list is represented, but instead of just showing the index, it will show the key and the value. 

At this point, our program will loop back to the start of the for loop. Since there are more iterations to complete, we'll update the iterator variable `i` to $1$, and then enter the loop again.

![Tutor 9](/images/lab14/tutor13_9.png) 

Once inside the loop, we'll add another item to the dictionary, and then loop back to the top. 

![Tutor 10](/images/lab14/tutor13_10.png) 

From here, hopefully it is clear what the rest of the program will do. Each time we enter the loop, we'll generate a new key and value pair to add to the dictionary. So, let's skip ahead to the end of the loop. 

![Tutor 19](/images/lab14/tutor13_19.png) 

At the end of the program, we'll print the contents of the dictionary to the terminal. Just like with lists, Python will print dictionaries in a clean and easy to understand format, as shown in the output in Python Tutor:

![Tutor 20](/images/lab14/tutor13_20.png) 

A full animation of this program is included below.

![Tutor 13](/images/lab14/tutor13.gif)

As we can see, dictionaries in Python work very similar to lists. When we create a dictionary, it is stored in the objects area in memory, and we can easily add, access, and even print the contents of a dictionary in our code. Dictionaries are really one of the most flexible data structures available in Python.