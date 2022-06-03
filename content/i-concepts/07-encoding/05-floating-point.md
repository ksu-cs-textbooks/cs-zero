---
title: "\u2705 \u2705 Floating Point"
pre: "7.5 "
weight: 20
date: 2020-08-28T16:27:26-05:00
---

{{< youtube LqH8uSuDb-s >}}

<!-- CIS 115: q9_cGKpIbm0 -->

#### Resources
* [Slides](../slides/7-Encoding.pdf)

#### Video Script

So far in this module, we've only dealt with whole numbers such as positive and negative whole numbers or integers. But what about numbers that have decimal points in them? How would we deal with those? In mathematics, of course, we call these rational numbers because they can be expressed as a ratio or a fraction. And so in mathematics, one thing that we've used for rational numbers would be scientific notation. You may have seen this a few times in your science class, you'll have numbers like 1.0 * 10^5.

In binary, we use a similar system that we call floating point. And the whole idea behind floating point like scientific notation is that the decimal point in the number can float around. And specifically, we can do something really cool where we can express a decimal number as two whole numbers, a mantissa, which is the value and then exponent, which is a power that is used to adjust the location of the decimal point. So this slide right here actually shows an example of what that looks like for scientific notation. And we do something very similar for binary numbers. 

Binary numbers use the system of floating point, which is based on the IEEE754 standard. And in this slide, I'm going to show you the 16 bit or half size example, which uses an exponent bias of 15, which we will understand in a little bit. Also, it's really important to understand that the leading one of the mantissa is implied. And again, we'll talk about that in a minute. In most actual computer systems, instead of a 16 bit number, you would have a 32, 64 or 128 bit floating point number, but that gets a little bit hard to do on a simple screen. So we'll use 16 bits, but the theory is very similar. 

So let's see what it takes to convert this floating point number into its equivalent decimal for so this example we have a 16 bit floating point number, and you notice it consists of three parts. The first bit is the assignment, and since the assignment is zero, we know that this is going To be a positive number, the next five bits are the exponent. This exponent is 10100. This exponent is equivalent to a decimal value, where we have one, two, this is four, so we have four 8, 16. So you have 16 plus four is 20. Now the important thing to remember is the exponent has a bias of 15. So when we're going from this value into its decimal value, we really have to take this binary value 20 minus 15, and we get an exponent of five. This allows us to actually store both positive and negative exponents using a positive binary number. For example, if we want to store the exponent, negative five, we would have negative five here and we would add 15 to it and we would get 10 And so then we will encode the binary value 10, which is 01010 as our exponent. But again, we're not doing that in this example. So we're going to erase that. And we know our exponent is five. 

The next thing we need is our mantissa. And so in the explanation, we saw that there is an implied one here at the front of the mantissa. So this mantissa is really the binary value 1.0101. Now there are two ways to think about this mantissa Of course, we can calculate it directly. And just like with decimal values, where items to the other side of the decimal point are divide our negative powers of that value, so this is two to the zero, so this would be two to the negative one to the negative two to the negative three and so on. So we can actually calculate this value As one plus one fourth plus one 16th. So we can actually calculate this value, one plus one fourth plus one 16th, which is approximately 1.3125. So we have the value 1.3125 times to the fifth. And we know that two to the fifth is 32. So if we take 1.3125 times 32, we will actually get exactly the value 42. So that is the actual decimal value of this floating point number. 

That may seem a little complicated, but there is actually a much easier way to do this. Recall that we started with the binary number 1.0101. And we know our exponent is five. So before we do any conversion, all we have to do is move this decimal place five places and so we end ended up with the binary value 101010 with the decimal place here at the end. And of course, we know that the binary value 101010 is equal to 42. So in calculating this value, a lot of people find it much easier to move the decimal place first, and then calculate the binary value, instead of calculating the binary value and then multiplying it times two to the fifth or two to the whatever the power is. Either way works, I have found the second way, much, much simpler. 

So as we saw with this example, we can calculate the value of the mantissa. And we can calculate the value of the exponent to be 1.3125, and five, so the overall value is 1.3125 times to the fifth, which is 42. Or we can take the binary value times two to the fifth and simply slide the decimal place over and we'll find the binary value 42. 

So let's do another example. This time converting a decimal number all the way to a floating point binary number to see what that process looks like. And in this case, let's do the value 86. We've already converted 86 to binary before, which was 1010110 with the decimal point right here, so we need to do two things. The first thing we need to do is move the decimal place all the way forward, so we need to move it 1,2,3,4,5,6 places, so our exponent is going to be six. So to find our actual exponent value, remember we have to add the bias which is 15. And we will get 2121 in binary is going to be 16 plus four, plus one. So we get the binary value 10101. Then to construct our actual floating point number we start with our sign bits. So we have our sign bit right here, this is going to be zero, then we'll have our exponent which is going to be 10101. And then we will have our mantissa. And remember with the mantissa, we take this value, but we remove this one off of the front, and so the mantissa will be 010110. And then we will fill the rest of it out with zeros until we get to 16. So we have There we go. So the decimal value 86, we can easily convert to a floating point binary number by moving the decimal six places using that six to calculate our exponent of 10101 and then calculating the rest of the mantissa by taking the one off of the value and using the other bits in the mantissa.

Floating point numbers can have a very, very wide range of values. For example, the 16 bit binary floating point numbers that we looked at today have a range from negative 65,000 to positive 65,000 in whole numbers, but it can actually show values as small as 5.9 * 10^-8 And it also has ways of showing positive infinity and negative infinity by setting the exponent to all ones and setting the mantissa to all zeros. Unfortunately, because it is a rational number, it is inexact. For example, if we want to show the value one third, we would end up with this binary floating point of 0101010101 in the mantissa, which is really just 0.33325, which is not exactly one third, just like one third is a repeating decimal in decimal values. One third is also an infinite repeating binary floating point number as well. So it can't be exactly shown, but it's not really Either 0.3325 is actually pretty close to what we want. So what are these numbers look like in a real world computer in most modern operating systems and integer is a standard size of 32 bits, although most normal processors today actually support 64 bit integers by default, but a lot of programming languages are still built around the idea of 32 bit numbers. Likewise, we can have long integers which are 64 bits. And then for floating point we have half size, the single size or float which is 32 bits and the double size floating point which is 64 bits. And here we show that of these 32 bits, eight of them are used for the exponent and 23 are used for the mantissa. Likewise for a double size 11 bits are used for the exponent and 52 bits are used for the mantissa