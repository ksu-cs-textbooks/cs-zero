---
title: "Introduction"
pre: "1.1 "
weight: 5
date: 2020-08-10T16:27:26-05:00
---

{{< youtube WRI9Jvoo6V4 >}}



#### Resources
* [Slides](../slides/01-What-is-Computing.pdf)

#### Video Script

##### Introduction (Slides 1-3)

In this course, we're going to ask ourselves, what is computing science? It's a really important topic that we'd like to cover throughout this course. But it's also one that's very difficult to understand. So when we try and understand the topics such as what is computing science, we can ask ourselves the questions: who? what? when? where? why? and how? And while I do this, I realized the question of "how" is really the best way to approach computing science. Specifically, I like to think of computing science as the study of how - how we can make things faster, better, more efficient, more accurate and more secure using computers. But that becomes a really interesting statement because we haven't discussed exactly what a computer is. 

##### What is a Computer (Slides 4-7)

So before we can look at all this "how", let's ask ourselves: "what is a computer?" We're all probably familiar with the modern computers that you and I have in our homes and around us today, but is that really the best definition of what a computer is? Or is there more to it? That's what we're going to take a look at in this video. So to really understand what a computer is, we have to go back a little bit and look at some of the earliest examples of devices that might be considered a computer. And it turns out those devices are really wrapped up in the history of mathematics. 

So on this slide, we see some mathematical equations, such as the equation for the exponential function, which is this long, repeated division. We can have sine and cosine and all of the trigonometric functions. We can have limits which are the basis of calculus, and we can even have logarithms which show up a lot in statistics and finance. And all of these functions are very, very difficult for people to calculate by hand. So how do we find the values of, for example, sine of 46 degrees? Using modern technology, we can find these values using some very interesting tools such as computers or calculators, but in the 1600s, they might have to use something such as this. 

This is a book of math tables from 1619, and it gives the value of sine, tangent, secant for all sorts of different angle values. And so a table such as this might be used by engineers, mathematicians and scientists whenever they need to find these values for their work. And in fact, if you've taken a calculus class, or trigonometry class or geometry class, your textbooks probably had tables like this in the back of the book. And as recently as the 1960s and 1970s, engineers would have had little books full of these tables that they carried with them all the time before the rise of the modern pocket calculator. But of course, this begs the question of how do we get these numbers in these books? We don't have computers, we don't have calculators. 

So how did we do it? And it turns out that that lies in the work of a lot of early mathematicians such as John Napier, who helped describe the logarithmic function, and Jacob Bernoulli, who helped describe the exponential function. And so one way that you could populate a book full these values is work with the best mathematicians at the time and have them perform all of that mathematical work. And this is important because in the 1600s, not many people had the level of mathematical training required to work with those really complex functions that we saw earlier. But of course, this is not a really great use of their time. So we tried to find ways where we could do better and easier mathematics to find those complex values. 

##### Divided Differences (Slides 8-10)

One of those big improvements was the creation of Taylor series. If you ever take a calculus class, you'll learn all about Taylor series. But the big thing to understand is a Taylor series is simply an infinite polynomial that expresses values of those complex functions. For example, the exponential function can be expressed as the infinite polynomial, one plus x plus x squared over two factorial plus x cubed over three factorial. And so we've reduced this value down to a set of individual terms. And so if we can calculate the value of each individual term and add them together, we can find the values for the exponential function. Of course, this is a little bit easier than that earlier statement, but it's still very, very complex mathematics that would take a lot of work. 

Enter the work of Sir Isaac Newton, Isaac Newton, you've probably heard of lots of times in your math and science courses, and he was very impactful in a bunch of different fields. But for this particular field, we're looking at one specific thing he created that's not very well known, which is the method of divided differences. And so Newton's method of divided differences allows you to find successive values of a polynomial, any sort of polynomial that you can create, including these infinite polynomials for Taylor series. You simply cut them off at a particular value, and then you use that polynomial and Newton's method of divided differences to find those values that you would place in a book. So let's look at an example of Newton's method of divided differences to see how it works. 

To understand Newton's method of divided differences, we have this example with a polynomial: two x squared minus four x plus three. Then we've created a table below, where we have the first column that gives values of x and the second column that gives values of the polynomial applied to that value of x. So for example, if we put x equals zero into the polynomial, we'll get the value three. If we put x equals one in the polynomial, we'll get two minus four plus three, which is one, and so on. So we can populate the first few values in this polynomial column very easily using simple mathematics. 

Once we've got a few of those values, then we can build this first differences column. And so the differences column will take the value of the polynomial at one minus the value of the polynomial at zero, and so we'll have one minus three, which will give us negative two. Likewise, for the next value, we'll take three minus one, and we'll get the value two. And so we can do that to fill out the first few values in this difference column. 

And then we'll do it again to make a second difference column. So here we have two minus negative two, which is for. And what Newton realized is if you do this enough times, you'll eventually reach a column where all the values will be the same. And you have to do that for each order of the polynomial. So this is a polynomial of order two. So that means we need two division, or two difference columns to get to this column, where all the values will be the same. So now, once we know that this column is four, we can put in four for each of these values. 

And then we can use those to work forwards through the table to find other values of the polynomial. So now to fill out this value right here, we can do four plus two, and we'll get six. Then we can do four plus six to get 10 here, then we'll do four plus 10 to get 14, then we can work forward again and fill out the polynomial column where we have six plus three is nine. 10 plus nine is 19, and 14 plus 19 is 33. There we go. That's how you do Newton's method of divided differences. 

This slide shows a completed table that is a little bit easier to read. And we can see that we got the correct values. Now this method of divided differences does have one major issue, and that is it's very susceptible to human error. For example, what if we add four plus six and instead of getting 10, we get 11. Then what happens? Well, if we do four plus 11, here, we'll get 15 instead of 14. Then if we do six plus three, we get 9, 11 plus nine, now we will get 20 here. And then likewise, if we do 20 plus 15, instead of 33. We will get 35. And so as you can see, by making one small error right here, we've actually made all of the subsequent values in the table invalid. And that's the real problem with Newton's method of divided differences. As soon as you make one error, it invalidates everything after it. So while it's a very powerful tool, it still has a big weakness. 

##### Charles Babbage (Slides 11-12)

And the real idea is how can we solve this weakness. And that was of interest to Charles Babbage. Charles Babbage was an inventor and a mathematician in England in the 1800s. And he was really interested in creating ways that we could perform these repeated calculations without the risk of human error. And he decided that it was possible to build a mechanical device that could perform these mathematical operations completely, repetitively without any error. And during his lifetime, he actually built a small prototype of this device that he called The Difference Engine, and he built blueprints for a much larger scale version of it, but that version was never actually completed during his lifetime. A few years ago, those blueprints were in the possession of a Computer History Museum and they decided to try and build a device based on his blueprints and see if it would actually work. And surprisingly enough, it totally worked. So let's take a look at a video of that completed Difference Engine that was built by a Computer History Museum and see how it works. 

