---
title: "Print Statement"
pre: "9. "
weight: 90
date: 2021-01-15T00:00:01-05:00
---

{{< youtube yveXTTVXzZ0 >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

The first statement that we'll cover in the Python programming language is the `print(expression)` statement. This statement is used to display output to the user via the terminal. So, when Python runs this statement, it will evaluate the `expression` to a single value, and then print that value to the terminal. 

For example, the simplest Python code would be a simple Hello World program, where we use the `print(expression)` statement to display the text `"Hello World"` to the user:

```python
print("Hello World")
```

When we run that program in Python, we'll see the following output:

```tex
Hello World
```

Just like in pseudocode, strings in Python are surrounded by double-quotes `"`. For now, we're just going to work with string values, but in a later lab we'll introduce numerical values and discuss how to use them as well.

Let's go through the full process of writing and running that program in Python!

## Writing a Python Program

The first step to create a program in Python is to create a text file to store the code. This file should have the file extension `.py` to indicate that it is a Python program. So, we'll need to create that file either on our computers or in Codio or another tool if we are using one. For example, in Codio we can create the file in the `python` folder by right-clicking on it and selecting the **New File** option. We'll name the file `hello.py`:

![New File](/cc110/images/lab3/new_file.png)

Once we've created that file, we can then open it by clicking on it. In Codio and in other online tools, it will open in the built-in editor. On a computer, we'll need to open it in a text editor specifically designed for programming. We recommend either [Atom](https://atom.io/) or [Visual Studio Code](https://code.visualstudio.com/), which are available on all platforms. Tools like the built-in Notepad tool on Windows, or a word processor like Word or Pages do not work for this task.

In that file, we'll simply place the code shown above, like this:

![Code](/cc110/images/lab3/code.png)

That's all there is to it!

## Running a Python Program

Once we've written the code, we can open the **Terminal** and navigate to where the code is stored in order to run the program. On Codio, we'll just use the `cd python` command to enter the `python` directory. On a computer, we'll need to navigate the file system to find the location where we placed our code. We highly recommend creating a folder directly within the home directory and placing all of our code there - that will make it easy to find!

Once we are in the correct directory, we can use the `ls` command to see the contents of that directory. If we see our `hello.py` file, we are in the correct location:

![Show Python File](/cc110/images/lab3/file.png)

If we don't see our file, we should make sure we've saved it and that our current working directory is the same location as where the file is stored. 

Finally, we can execute the file in Python using the `python3` command, followed by the name of the file:

```bash
python3 hello.py
```

If everything works correctly, we should see output similar to this:

![Hello World Output](/cc110/images/lab3/hello.png)

There we go! We've just run our first program in Python! That's a great first step to take. 

Of course, there are lots of ways that this could go wrong. So, if you run into any issues getting this to work, please take the time to contact an instructor and ask for assistance. This process can be daunting the first time, since there are so many things to learn and so many intricacies we simply don't have time to cover up front. Don't be afraid to ask for help!