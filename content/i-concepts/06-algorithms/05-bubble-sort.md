---
title: "Bubble Sort"
pre: "6.5 "
weight: 20
date: 2020-08-10T16:27:26-05:00
---

{{< youtube slWeGcRnBGI >}}

<!-- old 1RlwugeE4Dw -->

#### Resources

* [Slides](slides/6-Algorithms.pdf)

#### Video Script

The next algorithm we're going to look at is bubble sort. Bubble sort might seem similar to Insertion Sort, but it's actually quite the different algorithm. So in bubble sort, what we will do is we will start by comparing two side by side elements in the list of data. And then if they're out of order, we will swap them. You can see in the animation above me how those two red boxes move to compare two side by side items. And if they're out of order, it will swap them just like so. Then we'll repeat that once we get all the way to the end of the array. We'll start back over at the beginning, and we'll go through it multiple times until it is entirely sorted. Or as the algorithm says here, we'll continue until we go all the way through the array and we don't make any more swaps. So let's go take a look at how to perform bubblesort using our deck of cards. The next algorithm we will look at is the bubble sort algorithm as we do bubblesort keep track of how many times you swap to different cards as that will become really important as we analyze these algorithms later on in this module. 

So to do bubblesort, we start off by looking at the first two cards, the seven and the eight. And we ask ourselves are these two cards out of order, the seven should come before the eight. So we know that these two cards aren't out of order, so we won't do anything. Then we will shift one position over and look at these two cards, the eight and the four. And once again, we ask ourselves are these two cards out of order, the eight shouldn't go before the four. So they're out of order, and they need swapped. So that's one swap that we have done so far. Now we'll look at the eight and the two, we see that those are out of order. So we'll swap those that's two swaps. The eight also goes after the ace. So that's three stops, swaps. Then we have the eight goes after the three, which is four swaps. Now we're looking at the eight and the 10. And in this case, the eight does go before the 10 so We won't do anything here. 

Now we'll look at the 10 and the nine, and we see that those are out of order and need swapped. And likewise, the 10 goes before goes after the six, and goes after the five. And so now we've made it all the way through our list of cards. And we noticed that the highest card, the 10, has bubbled to the end of the list. And that's the really important part about bubblesort. Each time you go through, at least one more card should be bubbled to the correct spot at the end. So once we've made it to the end, we'll start all the way over here at the beginning and try it again. So now we look at the seven and the four. Those are out of order and need swapped. We'll look at the seven and two. Those needs swaps. The seven in the ACE get swapped the seven and the three gets swapped, but now the seven and the eight don't get swapped. Likewise the eight and the nine are in the correct order, but the nine in the six are out of order. Needs swapped, and the nine and the five are out of order and need swaps. 

So now we've made it through twice. And we now have two cards, the nine and the 10 that have bubbled to the end of the array been placed in the correct order. So now we'll repeat this process once again, we see the four needs swapped with the two, the four and the ace needs swapped the four and the three needs swapped, the four and the seven are okay, the seven and the eight are okay, the eight and the six need swapped as well as the eight and the five. So now we have the eight in the right spots. We'll start over again. We'll put the ace in the two, the two and the three, right, the three and the four, right, the four and the seven are right, but the seven and the six are out of order. And the seven in the five are out of order. And now we have four cards in the right spot. And if we start over again, we'll notice the ace and tour Okay, two and three are okay, three and four. Okay, the four and the six are okay, but the six and the five out of order. And now we have five cards in order here. But look, we've already got the array sorted even though we still had a few cards that we weren't sure about. 

We know that if we went through it again, we would not make any swaps. And that's one of the powerful features of bubblesort is that once we make it all the way through our list of numbers without making a swap, we know that it's in the correct order, and we can stop working. See if you can do the bubble sort algorithm on your own using a deck of cards to understand how this algorithm works. And remember, while you do that, keep track of how many times you have to swap two numbers because that will help us in our analysis in the next video.