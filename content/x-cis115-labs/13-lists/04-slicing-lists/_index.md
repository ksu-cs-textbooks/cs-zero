---
title: "Slicing Lists"
pre: "4. "
weight: 40
date: 2021-04-10T00:00:01-05:00
---

{{< youtube  >}}

#### Resources

* <a href="{{<relref "./slides">}}" target="_blank">Slides</a>

One of the coolest features in Python is the ability to easily create **slices** of lists. A **slice** is simply a portion of a list that can be stored and used as a separate list, allowing us as programmers to quickly create and manipulate new lists based on existing lists.

There are two basic ways to create a list slice in Python.

1. `nums[start:end]` - this will create a slice of the list stored in `nums` that begins as the index `start` and ends before the index `end`. For example, if `nums` is storing the list `[2, 4, 6, 8, 10]`, then `nums[1:3]` would create the list slice `[4, 6]`. 
1. `nums[start:end:step]` - this will create a slice of the list stored in `nums` that begins as the index `start`, moves `step` indexes between each successive items, and ends before the index `end`. For example, if `nums` is storing the list `[2, 4, 6, 8, 10]`, then `nums[0:5:2]` would create the list slice `[2, 6, 10]`. 

The method for creating list slices is very similar to how the `range()` function is used in Python. In effect, if the same values are provided as arguments to the `range()` function, then it will produce the list of indexes that will be used to generate the list slice.

Beyond the simple syntax, there are a few other rules to understand about list slices:

1. Any of the numbers may be omitted, as long as there is at least one colon placed inside of the square brackets. By default, `start` will be $0$ at the start of the list, `end` will be the size of the list, and `step` will be $1$. So, each of these are valid ways to slice a list, and there are many more possible combinations:
    1. `nums[:]` - this will effectively copy the list and include every item in the slice.
    1. `nums[start:]` - this will include all items in the list starting at `start`.
    1. `nums[:end]` - this will include all items in the list before `end`.
    1. `nums[::step]` - this will include all items in the list starting at index $0$ and moving forward `step` indexes each 
1. List slices may include negative indexes! In fact, we can use negative indexes to access elements in any list in Python. Some examples:
    1. `nums[-1]` - this will access the last item in the list
    1. `nums[-3:]` - this will create a slice containing the last three items in the list. 
    1. `nums[:-2]` - this creates a slice of the entire list except for the last two items. 

For example, we can start with a simple list, and then try the various list slicing methods to see what elements would be included in the new list. Here's an example program that shows some of the various ways to manipulate lists in Python:

```python
def main():
    nums = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    print(nums)

    # simple slices
    print(nums[3:7])
    print(nums[5:])
    print(nums[:5])
    print(nums[::2])
    print(nums[1::2])

    # negative numbers
    print(nums[-1])
    print(nums[-7:-3])
    print(nums[-3:])
    print(nums[:-3])
    print(nums[::-1])


main()
```

When we execute the program above, we should see the following output:

![Output 2](/images/lab13/output2.png)

List slicing is a great way to use and manipulate lists in Python, but it takes a bit of practice to learn all the various ways that it can be used. Feel free to play around with all of the various examples above using some sample data to see how they work. 

{{% notice note note-1 "Create List from Range" %}}

The `range()` function in Python is used to generate a list, but unfortunately we can't directly use that list in our code without a bit of manipulation. For example, we can try to store the result of the `range()` function in a variable as shown here:

```python
nums = range(10)
print(nums[3:7])
```

However, when we try to run that code, we'll see this output:

```tex
range(3, 7)
```

This is because the `range()` function doesn't actually create a list - it is it's own data structure type! Since a range can be constructed from just three numbers, it is much simpler to store just those numbers in memory instead of the entire list of numbers that it represents. When we create a slice of a range object, it just generates a new range instead of a list. So, to actually convert a range to a list, we must use the `list()` function in Python:

```python
nums = list(range(10))
print(nums[3:7])
```

This will produce the expected output:

```tex
[3, 4, 5, 6]
```

You can learn more about this by reading Python's [Range](https://docs.python.org/3/library/stdtypes.html#range) documentation. 

{{% /notice %}}