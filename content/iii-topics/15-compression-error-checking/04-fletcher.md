---
title: "Error Checking - Fletcher's Checksum"
pre: "15.4 "
weight: 20
date: 2020-10-16T00:27:26-05:00
---

{{% notice warning "Errata" %}}

_The C2 total on the slide at 0:54 - 2:10 is incorrect. The total is `7336` but that value modulo `255` is `196`, not `96` as shown in the video._

{{% /notice %}}

{{< youtube 9bagsZQa3Cs >}}


#### Resources
* [Slides](slides/15-Compression-Error-Checking.pdf)

#### Video Script

Let's look at an even better way to do a checksum to check and see if our data is correct. This is called Fletcher's checksum. And here we're giving a quick pseudocode of the algorithm that is used to generate Fletcher's checksum. Basically, the way it works is you divide the word into a sequence of equally sized blocks. And we'll just use the individual characters for this. And we'll start with two checksums, one of them, C1 starts at zero, the other to also starts at zero, then for every block, we'll add the value of the block to the first check sum. And then we'll add the new value of that checksum to the second checksum. And then finally, while we're done, we will calculate the values of the checksum mod 255 to reduce them to an eight bit binary value. And we'll return those two checksums. 

So let's take a look at an example of how we would do Fletcher's checksum. We'll start with our same messages always and divided into blocks where each character is its own block. So the first character, the capital H is a value 72. So we'll add 72 to the first checksum. And then we will add that checksum value to the second checks up. So after the first character, they're both the same. The second character, the lowercase E is 101. So we'll add 101 to the first checksum to get 173. But now we will add this new checksum 173 to the value of 72 and the second checksum to get 245. Likewise, we'll add 108 to 173 to get 281, then we'll add 281 to 245 to get 526. And we'll continue this process until we've done all the letters. And then at the end, you'll see that we still get the same checksum that we found earlier 1101, which becomes 81 when we do mod, and then the second checksum becomes 7336, which is 96 when we do them on. So now we only have to send along two additional numbers along with our text. And that will tell us a lot more about the text in the errors. So let's take a look at that and see how many errors this can find. Let's consider the case of just doing these first three characters. So we know that the checksum for 72, 101 ,108. If we look back here should be 281 and 526. So we would have 281 and 526. So let's look at this first example. We have 72 108 101. Well, that changed the first checksum? No, it's the exact same value, it will be to 81. However, will it change the 526? Well, we start with 72. And then we will add 72 plus 108, which is going to be eight 180. So the second check sum will be 180. So we're going to add 180 here, 180 here, which is going to be 252. And then to the 180, we're going to add 101. So the second checksum is still going to be 281. But if we add 281. Here, we're going to get 331, we get 533. 

So in this example, by switching these two characters, the first checksum did not change, but the second checksum definitely changes. And that's because the order changed. Likewise, when we look at all of these examples, we see that all of them add up to the same set of characters. So the first checksum will always be 281. But the second checksum will be different every single time. And that's because we're adding this first checksum to the second checksum every single time so it captures the ordering of the characters as well as the values that they may change based on those different values. So even by adding a zero in there, we would get a different value for that second checksum. So once again, there will be a quiz after this video where you can try a little bit of Fletcher's checksum just to see how it works.
