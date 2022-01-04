---
title: "Complexity"
pre: "6.5 "
weight: 25
date: 2020-08-10T16:27:26-05:00
---

{{< youtube Fiein5rZ-6M >}}

#### Resources

* [Slides](/1-cc110/06-algorithms/slides/6-Algorithms.pdf)

#### Video Script

So far, we've looked at two different algorithms for sorting decks of cards, Insertion Sort, and bubblesort. So let's take a minute and try and decide which of those algorithms do you think is faster for a computer? a better question might be, which of those two algorithms was faster for you as it person to perform? Those are really tough questions to answer, aren't they? And so we need some way that we can analyze our algorithms and compare them apples to apples to see exactly which algorithm might be faster or more efficient on a computer. To do that, we use something called Big O notation. Unfortunately, when I refer to big O notation, I'm not talking about the giant robot anime from the early 2000s. Instead, I'm talking about the notation that we use to express the complexity of an algorithm. And specifically when we talk about complexity, we're talking about the number of steps required to perform the algorithm based on the worst case size of the inputs. 

To understand worst case, let's consider the instance of bubble sort. So here are five different lists of cards that we could give as input to bubble sort. And let's say we want to sort them from two all the way on the far side to the ace over here on the near side. So the final order would be 2,3,4,5,6, all the way up to 10, jack, queen, king, ace. Looking at these five inputs, which one do you think would be the worst case for bubble sort. So of course, we can analyze this. And if we count the steps required to perform bubble sort, we'll find that the fourth input is the worst case. And if we look closely at that output, we see something very unique. It turns out that that output is actually the deck of cards sorted completely backwards. And so that means that every step it would need to swap two cards that are out of order. So the first time through is bubble sort. We will bubble the ace all the way up to the end, which will require 12 swaps. Then the king which will be 11 swaps, then the queen, which will be 10, then nine, then eight, so on all the way until we get it sorted. And if we add that all up, it turns out that we make 78 swaps in order to sort that deck of cards. 

So the important part of big O notation is not finding that for a specific input, but finding that answer for a number of inputs and then graphing them. So this is a graph that shows along the bottom the size of the input in terms of the number of cards, and on the side, we have the number of steps that it takes to perform bubblesort. And so if we look at that graph, where there is 13 at the bottom, which is one suit of cards, we can go up and we see that 78 is about where that is. So if we look at this line, what sort of a function would we use in mathematics to create this line. As it turns out, this line follows the polynomial x^2. So we would say that insertion sort and bubblesort both run in big O of n^2. That means that for every n inputs, we expect it to take around n squared steps in order to solve the problem. Now you'll notice that there are two more algorithms on this slide that we haven't talked about yet. mergesort and quicksort. 

Do you suppose that there is a way that we can sort a deck of cards that is faster than big O(n^2)? A good way to think of n^2 is n^2 means that we would take every card and compare it to every other card in times in which is n squared. Can we do that faster? Let's take a look at mergesort and quicksort. And see if that's possible.
