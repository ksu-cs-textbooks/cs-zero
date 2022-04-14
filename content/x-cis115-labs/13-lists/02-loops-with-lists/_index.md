---
title: "Loops with Lists"
pre: "2. "
weight: 20
date: 2021-04-10T00:00:01-05:00
---

{{< youtube SOz8zKt2jnU >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

One great way to work with lists in Python is using a loop. Recall from an earlier lab that a for loop actually iterates over a list itself, and that the `range()` function is simply used to generate a list that the for loop can use. Likewise, while loops can also be used in a similar way. 

Let's look at a quick example of how we can iterate through the items in a list using a loop in Python.

## For loop

Consider the following example program in Python:

```python
def main():
    nums = [3, 1, 4, 1, 5, 9, 2]
    print("The first seven digits of pi are...")
    for i in nums:
        print(i)


main()
```

In this example, the for loop will iterate through the values in the `nums` list instead of a given range. So, during the first iteration, `i` will store the value $3$, then $1$, then $4$, and so on until it reaches the end of the list. When the program is executed, we should receive this output:

![Output 1](/images/lab13/output1.png)

Using a list in a for loop is an excellent way to go through each element quickly, and it allows us to build for loops that don't require the use of the `range()` function to generate a list that is in some sort of sequential order. We'll see this pattern used very often in our programs using lists.

Finally, it is not recommended to edit the contents of the list while inside of the for loop using this method. Since we are only getting the individual values from each list element, we cannot easily make changes to the list itself without causing issues in the loop itself. Instead, if we want to make changes to the list while we are iterating through it, it is highly recommended to use a while loop structure as shown below. 

## While Loop

It is also possible to iterate through a list in Python using a while loop. However, instead of iterating through the items themselves, we can use an iterator variable that references the indexes of the elements in the list. Consider this example program:

```python
def main():
    nums = [3, 1, 4, 1, 5, 9, 2]
    print("The first seven digits of pi are...")
    i = 0
    while i < len(nums):
        print(nums[i])
        i = i + 1


main()
```

This program is effectively the same as the one above, except that it uses a while loop to iterate through the items in the `nums` list. We start by setting the iterator variable `i` to be $0$, the first index in the list. Then, in the while loop, we use the special `len()` function, which is used to find the size of the list. Since the list contains seven items, the length of the list is $7$. Another way to think about the length of the list is that it is always one more than the highest index - if the last item in the list is at index $6$, then the length of the list overall must be $7$. 

Then, inside of the loop, we'll use the iterator variable `i` inside of square brackets to access each individual element in the `nums` list and print it to the terminal. We'll also need to remember to increment `i` by one each time. 

This method is very useful if we want to do more with the list inside of our loop, such as edit individual elements or make changes to the overall structure of the list. This works because we can directly manipulate the value in the iterator variable `i`, and then use it to access individual elements in the list and update them. Also, if the size of the list changes, it will be checked using the `len()` function after each iteration of the while loop.

So, as a general rule, we should use a for loop when we just want to iterate through the list and not make any changes to the list while inside of the loop. If we do need to make changes, it is better to use a while loop and an iterator variable to access the list elements directly. 