---
title: "Compression - Huffman Coding"
pre: "15.2 "
weight: 10
date: 2020-10-16T00:27:26-05:00
---

{{< youtube CIfZPdFi2Ns >}}


#### Resources
* [Slides](/1-cc110/15-compression-error-checking/slides/21-Compression-Error-Checking.pdf)

#### Video Script

Next, let's take a look at another form of compression called Huffman coding. Huffman coding uses the frequency of the letters in a piece of text to reduce the amount of space that they take up in the encoded data. To do this, we will count the occurrences of each character in our text. And we'll use that count to make a binary tree with the data. Then the paths of the tree to each character give the codes that we use for the Huffman encoded data. This is a little bit complex. 

But let's take a look at an example and see how this works. Let's say we'd like to send this particular text using a Huffman tree. This is an example of a Huffman tree. If we count this just as plain ASCII characters, it would take 298 bits, which is 8 times 36 characters to send this data. So now let's look at how we would encode it into a Huffman tree. The first thing we would do is we would count the number of occurrences of each character. 

So let's look at an example of how we would convert this into a Huffman tree. The first thing we would do is we would count the frequency of each character. So let's take a look at the spaces we have 1 2 3 4 5 6 7. So we have seven space characters in this particular example, so we can make a list. On this slide, we see the list of some of the most common characters in that text. There are seven spaces, 4 letter A's, 4 letter E's, 3 F's, 2 H's, 2 I's, 2 M's, 2 n's, and so on. 

So with that data, we can then construct a binary tree by using the frequency of the characters to determine where they go in the binary tree. Since the space is the most frequent character, we're going to put it at the very top of the tree, whereas least frequent characters, for example, a p would go toward the bottom of the tree. So if we follow the Huffman example algorithm, we'll see that we create a binary tree that looks something like this. And this is pretty complex. And we're not going to exactly talk about how to build this binary tree. But there is a very unique algorithm that you'll learn about later on that can allow you to do this. 

So now we look at this tree. And we see that the space character is way over here. We mark it for you. So the space characters right here. So to get to that space character, we will make right, here, right here, and right here. So the space character, in terms of directions would be RRR. Likewise, the E, we would go left, left, left. So E is going to be left, left left. This is the space, this is the E. And so in Huffman coding, we would use the direction that we go in the binary tree to become our data. So if we encode this, so that right is ones, we would do 111 for the space, for the E, it would be 000. Pretty cool, isn't it? 

Likewise, if we want to get to the letter A, we would go left, then right, then left, so A would be left, right left to get A. So that would be 010. Pretty cool, isn't it. So we've taken characters that normally need eight binary values to represent them. And we can represent them here with this tree in anywhere from three to five characters. So if we look at this Huffman example, broken up, we'll see something like this, the letter team becomes 0110, H is 1010. And if we go on, we can eventually find the A, which is going to be this one right here, th, this, space, is, space, A n, space, example, we saw that he was 000. So right here, we've got a really big improvement. We've gone from 288 bits of data all the way down to 135 bits of data. So we've nearly cut it in half a little bit more than half actually, to make this work. 

Now, of course, Huffman trees do come with one particular caveat that we have to talk about. If we want to transmit this data encoded using a Huffman tree, we would also have to send a representation of the Huffman tree itself to allow this data to be decoded. And that can add a significant amount of overhead on small texts like this. In fact, the amount of data we would need to send this Huffman tree would be way more data than we needed to encode the original message even completely uncompressed. So while Huffman tree is a very powerful encoding system, It really works well when you're sending large amounts of text like an entire book, then using a Huffman tree to encode that you can get significant savings in your compression. So once again, we've got a little example of the Huffman tree encoding problem that you can try on the next quiz.