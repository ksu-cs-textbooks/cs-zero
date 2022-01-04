---
title: "Binary Numbers"
pre: "7.2 "
weight: 10
date: 2020-08-28T16:27:26-05:00
---

{{< youtube GL5DkDxb7xE >}}

<!-- CIS 115: -55ZMpP852Q -->

#### Resources
* [Slides](/1-cc110/07-encoding/slides/7-Encoding.pdf)

#### Video Script

The first thing we're going to cover in this module is the concept of binary numbers. Binary numbers are really the core of everything that a computer does. And so we need a way that we can convert the base 10 numbers that we know today such as 24 42 86, into binary numbers that only use ones and zeros. 

So let's start with simple natural numbers, the counting numbers, the whole numbers that are greater than zero. So let's take a look at this example. In here we have a binary number 00101010. And above that binary number we've put in the value of each place. So in a decimal number, each of these places would be powers of 10. So the first place would be one followed by 10 100 1,000, and so on. And so we know that the number 1234 would be 1, 234. 

In this number, however, we see that we only have ones and zeros, but they use the powers of two instead of the powers of 10 in each place. So let's look at how we can calculate the actual decimal value of this binary number. To calculate the value of a binary number, all we have to do is look for the places that have one. And then we know that this is one times 32. We have a zero here, so there's no value there. We have one here. So this is one times eight. We have a zero here, we have a one here, so this is one times two. Notice that this is the same thing that we do when we're using decimal numbers. Remember, the example I just gave 1234 would be one times 1000 plus two times 100 plus three times 10 plus four. So this value is 32 plus eight plus two, which is 42.

 At this point, if you are a fan of the work of Douglas Adams, you will find a definite pattern in the rest of this lecture, we're going to look at many different ways that we can encode the same number 42, in all sorts of different ways in our computer system. So as we saw with this example, it's really easy to take a binary number and convert it into its decimal value. All we have to do is multiply the ones by their place values in the binary number and then add the resulting number together to get the binary number. 
 
 What if we want to go the other way? How would we do that? For example, let's say we want to encode the number 86 as a binary number. To do this, we would have to again know our places are powers of two. So first, look at 128. Since 86, is less than 128, we know we can't have any values there. So we'll give that a zero. The next place would be 64. Since 86, is greater than 64. We know that we have at least one value of 64 in here, and now we'll have to do at Minus 64 and we will get 22. So now we go to our next power of two, which is 32, 32 is greater than 22, which means we'll give this a zero, then we will have 1616 is less than 22. So we get a one here, and then we'll subtract 16 and we will get six. So our next power is eight, eight is greater than six, we'll have a zero, then we'll have four, four is less than six. So we'll have a one here, and then we subtract four and we get two, then we'll have a two that is the same value. So we'll put a one and then two minus two is zero. So our ones place will have a zero. And so that tells us the binary number 01010110 is equal to the decimal number 86.