---
title: "Worked Example"
pre: "4. "
weight: 40
date: 2021-04-10T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

Now that we've explored how to create programs that contain nested loops, let's work through a complete example problem to see how we can convert a problem statement into working code.

Consider the following problem statement:

> Write a program to print the sum of the first `n` prime numbers, where `n` is provided as input from the user. 

This is a very simple problem statement, but it can be very complex to build a program that satisfies it. So, let's go through the steps and see if we can get it to work.

## Handling User Input

As always, we can start building our programs by adding a `main()` function and a call to the `main()` function to our code, as shown here:

```python
def main():


main()
```

Inside of the `main()` function, the first thing we'll need to do is get input from the user, since we really can't do anything else until we know what our goal is. While the problem statement doesn't include any information about what inputs are acceptable, we can infer that only positive integers should be used as input. So, we can borrow the `positive_input()` function from earlier in this module to handle all of our input:

```python
def positive_input():
    x = int(input("Enter a positive integer: "))
    while x <= 0:
        print("Invalid input!")
        x = int(input("Enter a positive integer: "))
    return x


def main():
    n = positive_input()


main()
```

Reusing existing code, such as the `positive_input()` function we just included here, is a great way to build our programs. We can always think of previous code that we've already written and tested as possible building blocks for future programs, and reusing existing code is a great way to speed up our development process.

## Prime Numbers

Next, we need some way to determine if a number is a prime number. Recall from mathematics that a prime number is a number that is only equally divisible by $1$ and itself. For example, $7$ is prime, but $8$ is not since it can be evenly divided by $4$. 

Thankfully, we know that we can use the modulo operator `%` to determine if a number if evenly divisible by another number. So, all we need to do is check if each number less than our chosen number can equally divide it. If none of them can, then our chosen number is prime.

So, let's write a function that performs this operation. We'll start by creating a function that accepts our chosen number as a parameter:

```python
def is_prime(n):

```

Next, we know that we need to check all of the numbers from $2$ up to but not including `n`. We can do this using a for loop and the `range()` function:

```python
def is_prime(n):
    for i in range(2, n):

```

Inside of the for loop, we want to check and see if the iterator variable `i` can evenly divide the chosen number `n` using the modulo operator:

```python
def is_prime(n):
    for i in range(2, n):
        if n % i == 0:
            # i equally divides n
```

Here's where things get a bit tricky - if `i` can equally divide `n`, we know that `n` is not prime and we don't have to check any other values. So, in our function, we can just use the `return False` statement to return the value `False` from this function. As soon as the function reaches a `return` statement, even if it is inside of a loop, it will immediately stop the function and go back to where it was called from. In effect, we can use this to **shortcut** the rest of the loop.

```python
def is_prime(n):
    for i in range(2, n):
        if n % i == 0:
            return False
    # what if we don't return false?
```

However, what happens if we check all of the values from $2$ up to `n` and don't find a single one that will equally divide our chosen number `n`? In that case, we'll reach the end of our for loop, but our function hasn't returned anything. So, we'll need to add one extra line to the end of the function to `return True` if we get to that point.

```python
def is_prime(n):
    for i in range(2, n):
        if n % i == 0:
            return False
    return True
```

There we go! That's a quick and easy function to determine if a given number is prime. This function is a great example of a pattern that we'll see many times as we write complex programs whenever we must determine if a particular situation is true for a given list of numbers. Inside of the loop, we'll check each case and return `False` if it isn't true. If it is true, then we'll complete the entire loop without returning `False`, so we'll need to return `True` at the end of the function. We'll see this pattern again in a later lab. 

{{% notice note note-1 "Efficient Prime Numbers" %}}

The `is_prime()` function above is very simple, but not very efficient. With a bit of thought, it is easy to determine that we only have to actually check numbers up to `n /2`, since it is impossible for any number larger than that to evenly divide `n`. Likewise, we can do some quick math to eliminate numbers that end in an even digit or $5$, since those numbers will never be prime. 

Finally, we could use a more advanced mathematical technique such as the [Sieve of Eratosthenes](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes) to generate all prime numbers more quickly. However, for this example, we'll stick to the simplest approach.

{{% /notice %}}

## Complete Program

Finally, now that we have the `is_prime()` function, we can complete our `main()` function by simply iterating through all possible numbers until we've found `n` prime numbers, and then print the sum:

```python
def main():
    n = positive_input()
    count = 0
    i = 2
    sum = 0
    while count < n:
        if is_prime(i):
            sum = sum + i
            count = count + 1
        i = i + 1
    print("The sum of the first {} prime numbers is {}".format(n, sum))
```

This program requires three additional variables. The variable `count` is used to keep track of the number of prime numbers found, so we'll increment it inside of the `if` statement each time we find a prime number. Likewise, the `sum` variable keeps track of the sum of the prime numbers, which we'll print at the end. Finally, we use `i` as our iterator variable, so we must make sure that we increment `i` each time the while loop iterates, outside of the if statement. We'll start `i` at $2$, since $1$ is not a prime number mathematically. A _very_ common programming mistake is to forget to increment `i` outside the if statement, resulting in an infinite loop. Also, we chose to use a while loop instead of a for loop since our program's goal is to sum up the first `n` prime numbers, which is better expressed as a while loop instead of a for loop.

The full program is shown below:

```python
def positive_input():
    x = int(input("Enter a positive integer: "))
    while x <= 0:
        print("Invalid input!")
        x = int(input("Enter a positive integer: "))
    return x


def is_prime(n):
    for i in range(2, n):
        if n % i == 0:
            return False
    return True


def main():
    n = positive_input()
    count = 0
    i = 2
    sum = 0
    while count < n:
        if is_prime(i):
            sum = sum + i
            count = count + 1
        i = i + 1
    print("The sum of the first {} prime numbers is {}".format(n, sum))


main()
```

Finally, notice that this program doesn't contain a loop nested within another loop in the same function, but because we are calling the `is_prime()` function, which contains a loop, from within a loop inside of the `main()` function, it actually has a nested loop structure inside of it! Feel free to run this program in Python or using Python Tutor to confirm that it works as expected before continuing.

## Testing

Testing this program is a bit complex, since we can only provide a single input. We can easily provide a negative value or $0$ to confirm that the loop in the `positive_input()` function is working correctly, but beyond that we have little control over the rest of the program just by changing inputs.

Instead, we have to rely on our ability to read and analyze the code to determine if it is working properly. For example, we can look at the loop inside of the `main()` function. It is a while loop, which relies on the `count` variable increasing until it is greater than or equal to `n` before it will terminate. We can see that `count` will be incremented each time the `is_prime()` function returns `True`, so as long as we are able to find enough prime numbers, and assuming our `is_prime()` function works correctly, this loop should eventually terminate. 

In the `is_prime()` function, we have a simple for loop, which will always terminate eventually. There is no way to bypass it, so we don't really have to worry about that function not eventually returning a value.

However, proving that this program creates the correct answer is a bit trickier. One of the best ways to do this is to simply check a few answers manually. For example, with a bit of searching online, we can find a list of prime numbers. According to [Wikipedia](https://en.wikipedia.org/wiki/List_of_prime_numbers), the first 9 prime numbers are:

```tex
2
3
5
7
11
13
17
19
23
```

The sum of those numbers is easy to calculate using a calculator or other device, and eventually we can be fairly certain that the correct answer is $100$. When we run our program, we should hopefully get the same result:

![Output 6](/images/lab12/output6.png)

We can test a few other numbers until we are sure that our program is working correctly.

Hopefully this example is a good look at how to build a program using loops that meets a given problem description. We were able to put together various types of loops and conditional statements in our program, and then test it to be sure it works. As you continue to work on projects in this class, feel free to refer back to these examples for ideas and blocks of code that you may want to use in your own programs. Good luck!
