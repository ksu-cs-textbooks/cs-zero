+++
title = "Shift Cipher"
date = 2022-04-17T00:23:05-05:00
hidden = true
pre = "<b>HW 5. </b>"
+++

## Shift Cipher

In this homework assignment, we're going to implement a simple shift cipher. In a shift cipher, each letter of the alphabet is replaced with a different letter in the alphabet, based on a _shift_ value. For example, a shift value of $1$ would convert the input `abcd` to `bcde` - each letter is replaced with the letter $1$ place further in the alphabet. Letters at the end of the alphabet are replaced with letters at the start, so a shift value of $1$ would replace `z` with `a`. 

The shift cipher is also known as the [Caesar Cipher](https://en.wikipedia.org/wiki/Caesar_cipher).

{{% notice note note-1 "Learning Objectives" %}}

The goal of this assignment is to demonstrate understanding of the following topics in Python:

* Lists
* Nested Loops
* Handling User Input
* Functions, Parameters, Arguments, and Return

{{% /notice %}}

## The Assignment

Write your program in a file named `homework5.py`, which will be uploaded to Canvas. This should be a **complete Python program** consisting of the following elements:

1. A `get_shift()` function
1. A `choose_option()` function
1. A `get_message()` function
1. A `create_key(shift)` function
1. An `encode(message, key)` function
1. A `decode(message, key)` function

Each function will be described in detail below.

## The Get Shift Function

The `get_shift()` function requires no parameters. It should prompt the user to input an integer value between 1 and 25, inclusive. If the user inputs an invalid value, the function should print an error and prompt for input again. When a valid input is received, it should return that value as an integer.

## The Choose Option Function

The `choose_option()` function requires no parameters. It should prompt the user to choose between "encode" and "decode" - it may ask the user to input a whole word, a single letter, a number, or any other reasonable method. If the user provides invalid input, the function should print an error and prompt the user for input again. When a valid input is received, it should return either the Boolean value **`true`** if the user chooses "encode" or **`false`** if the user chooses "decode"

**Pay close attention to the return type of this function!**

## The Get Message Function

The `get_message()` function requires no parameters. It should simply prompt the user to input a string to be encoded or decoded. The function should convert the string to lowercase using the `lower()` method on the string variable storing the user's input.

See the following example:

```python
text = input("Enter a message: ")
return text.lower()
```

## The Create Key Function

The `create_key(shift)` function requires a single parameter:

* `shift` - the value provided by the user and returned by the `get_shift()` function

The `create_key()` function should create a list of all $26$ letters of the alphabet that have been shifted by `shift` places. For example, if the `shift` value is $2$, then the list returned by this function should begin with `[c, d, e, f, g]` as the first five letters and `[x, y, z, a, b]` as the last five letters. 

One possible way to build this function is to import the `string` library and use the `string.ascii_lowercase` list to get all letters of the alphabet. Then, starting at the index `shift`, append sequential values from `string.ascii_lowercase` to a new list that makes up the key. You can use the modulo operator `%` to wrap back to the first index of the list once the index reaches $26$. 

See the worked example program in Lab 13 to see how to use the `string.ascii_lowercase` list.

## The Encode Function

The encode function requires two parameters:

* `message` - the text provided by the user in the `get_message()` function.
* `key` the key provided by the `create_key()` function

This function will encode the text stored in `message` using the key stored in `key`.

To encode a message, create an empty output message and loop through the characters in the input message one at a time and follow these steps:

1. Find the index of the character in the `string.ascii_lowercase` list.
1. Add the character at that same index in `key` to the output message.

If the character in the input message is not found in the `string.ascii_lowercase` list (such as spaces and punctuation marks), it should be added directly to the output message.

This function should return the created output message.

## The Decode Function

The decode function requires two parameters:

* `message` - the text provided by the user in the `get_message()` function.
* `key` the key provided by the `create_key()` function

This function will decode the text stored in `message` using the key stored in `key`.\\

To decode a message, create an empty output message and loop through the characters in the input message one at a time and follow these steps:

1. Find the index of the character in the `key` list.
1. Add the character at that same index in `string.ascii_lowercase` to the output message.

If the character in the input message is not found in the `key` list (such as spaces and punctuation marks), it should be added directly to the output message.

This function should return the created output message. 

## The Main Function

The `main()` function should call the other functions in the correct order to build the entire program. The basic outline is as follows:

1. Get the shift value from the user.
1. Use the shift value to build a key.
1. Ask the user to input a message to be encoded or decoded.
1. Ask the user to choose between "encode" and "decode".
1. Use either `encode` or `decode` to perform the desired action.
1. Print the resulting message to the terminal.

## Documentation & Comments

You may add any comments to your code to help explain how it works. In Python, you can use the hash symbol `#` (also known as a pound sign or octothorpe) in front of a line of text in a Python file to make it a comment:

```python
# This is a code comment
x = 15
y = 7  # comments can be at the end of lines, too
```

Your file should also include a **documentation comment**, also known as a **docstring** at the top of your file. The **docstring** should be formatted like this:

```python
"""
File Name: <filename>
Author: <your name>
Version: <submission date>
Section: <your section>
Description: <detailed description of this program>
"""
```

Notice that the start and end of the documentation comment uses three double-quotes `"""` on a single line.

## Sample Execution

Below is a screenshot showing several sample executions of the model solution for this homework assignment. Your submission should have similar functionality and output, but the text for input prompts may differ slightly:

![Sample Runs](/images/hw5/output.png)

## Submitting

Once you have completed this program, simply mark the unit as complete to submit it. Refer to the [Codio Documentation](https://docs.codio.com/students/#completing-assignments) for how to do this. 

{{% notice tip tip-1 "Variable Names" %}}

Be careful when naming your variables! For example, since we are using the `string` library, we cannot name any of our variables `string` since that would overwrite the library in our program. 

{{% /notice %}}