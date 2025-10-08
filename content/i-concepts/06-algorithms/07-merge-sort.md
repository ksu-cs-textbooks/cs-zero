---
title: "Merge Sort"
pre: "6.7 "
weight: 30
date: 2020-08-10T16:27:26-05:00
---

{{< youtube BJCQoZ5svhw >}}

<!-- old VCosBGaUpeA -->

#### Resources

* [Slides](slides/6-Algorithms.pdf)

#### Video Script

The next algorithm we're going to look at is merge sort. Merge Sort is a very unique algorithm because it's an example of the divide and conquer paradigm of creating algorithms. In fact, Merge Sort was actually written way back in the 1950s and 60s to allow us the ability to sort data that didn't even fit on a single data storage media at the time. So for example, with merge sort, we could sort the data on three different disks full of data very independently and very efficiently. The process for merge sort is pretty simple. We start by taking our data and splitting it in half, and we keep repeatedly splitting it in half until we get down to one or two items. Then we make sure those items are in order, and then we will merge those two items together all the way down until we get to our final results. So let's take a look at how we can perform Merge Sort using our deck of cards. The next sorting algorithm we'll look at is merge sorts. Remember that merge sort is a divided conquer algorithm. So it takes place in two phases. The first phase is the divide phase. 

So we'll start with our set of 10 cards, and we need to divide it in half. So we'll have one group of five cards over here. And we'll have one group of five cards over here. Then we'll repeat that process for each group. So we'll look at this group, and we'll divide it in half, we'll have a set of three cards, and a set of two cards. Likewise, here, we will have a set of three cards, and a set of two cards. And finally, these groups of three can be divided once again into a set of two and a set of one. And likewise here, we'll have a set of two and a set of one. So now we've divided all of our groups into sets that are at least two cards or smaller. The next phase is to actually sort each of these individual groups by swapping the cards If needed, so let's look at each group, the two and the four are out of order. And so we will swap them. So the two comes before the four. Since 10 only has one card, we don't do anything, the six and the nine are in the correct order, as are the three in the seven, the eight is all by itself, so we don't need to swap anything. And finally, the five and the ace are also out of order, so we will swap them. 

So in total, we only did two swaps, we only had to swap two of the possible four pairs of cards that we could swap, but that's all we really have to do. The last part of merge sort the conquer phase is where we merge all of these groups back together in sorted order. To do that, we pick two groups. And usually we just go down the row and we merge them back together by choosing the smallest card at the front of the group and putting it back in the destination. So with these two groups, we know that the two is the smallest. So it will go down first, then the four, then the 10. Likewise, we have this group over here, we know the three is the smallest, followed by the seven, followed by the eight. So now we have undone the division step that divided these into smaller bits. Now we'll do the merge step where we merge these two groups together, and these two groups together. So once again, we will look at the front card in each of our two and see which one's smaller. In this case, it's the two. So the two goes first, followed by the four than the six than the nine, and finally the 10. 

And so you can see that actually, a lot of the sorting happens in this merge phase more than anything else. Likewise, we can do the merge phase over here, where the ace will come first than the three, then the five, then the seven, and the eight. So we're almost there, we have one more set of merging that we need to do. And so once again, we'll look at the front card and each one, and we will see which one is smaller and merge it first, so the ace is smaller, so it will go first, followed by the two, then we'll have the three. Now we're looking at the four and the five, we take the four, the five and the six, we would take the five. Likewise, we would take the six before the seven than the seven before the nine, the eight before the nine. And then finally, the nine and the 10. Go here at the end. 

And so that's how we perform merge sorts. We divide everything out, we swap if needed, and then we conquer by doing that merge step to merge everything back together. And as we merge, we find that that's where a lot of the sorting happens by putting things back together using the front element, whichever is smaller until we get into sorted order. So once again, see if you can do merge sort on your own using Your own deck of cards and keep track of how many swaps you make and how many times you have to merge things back together. And we'll use that in our analysis in a later video.