---
title: "Introduction"
pre: "3.1 "
weight: 5
date: 2020-05-27T10:53:26-05:00
---

{{< youtube YYSFRGEAgdg >}}


#### Resources
* [Slides](../slides/03-Bits-and-Boolean-Algebra.pdf)


#### Video Script

##### Introduction (Slide 1-2)

For this lesson, we're going to be talking primarily about Boolean logic, Boolean algebra and how that plays into computer science and the foundations of how important that is and the role it plays and what we do. So before we get started, and before we can talk about things such as Boolean logic, we need to know where it came from. That leads us to Aristotle, way back in the 300 BC, as you may know, right Aristotle is one of the fathers of modern philosophy and logic among many other things. He studied under Plato, who himself was taught by Socrates and was also the teacher of Alexander the Great, so pretty much affected the entire world of Western philosophy that came after him. One of his major contributions was this idea of using formal logic to prove a point, then this form of logic, also known as Aristotelian logic, a point is proven based off of a series of premises. 

##### Aristotelian Logic (Slide 3)

For example, in this form of logic, we can present a series of facts. And so our premise here in that sense, all humans are mortal. Socrates is human. Each one of these is a fact and pretty easily proven to be true. Now, under Aristotelian we can use these use this premise to then prove a new fact. So if all humans are mortal, which is true, and Socrates is a human, which is also true, we can also prove or conclude that Socrates is also a mortal. 

##### Boolean Logic (Slide 4])

If we skip ahead a few thousand years later, we come to George Boole.  In 1854, he published a book called An Investigation of The Laws of Thought, in which he tried to apply the rapidly growing field of mathematics to the laws of logic. His goal was to reduce something as complex as logic to simple mathematical equations. And with the right rules in place, even a complex logic Statement could be completely proved, or even disproved using the same algebraic techniques they used to understand other parts of the world. 

And so if we take a look at an example, our same style of facts that we had before now transcribed into something that is more easily represented in algebra or mathematics, so for example, if we take are all humans are mortal and Socrates is a human, we can map that to different variables. And you can kind of imagine different kinds of facts being transcribed here where we can substitute proven facts or true facts in places of a and b and c, we can conclude new facts or new premises or new things from that. So if A and B so the upside down would be their means and we'll talk about that here in just a little bit. But if both A and B are true, and B and C are true, we can conclude that A and C is true.  Since A and B are true, B and C are true, then A and C must also be true. But this translation is somewhat flawed but we can leave that for a later course in logic or philosophy to describe why ...but let's take a deeper dive into what each of these mean so primarily Boolean operators Boolean values and what that means for Boolean logic. 

##### Boolean Values (Slide 5)

As you know from the reading computers operate primarily using only binary values so ones and zeros and Boolean logic and Boolean algebra operate off of true and false principles or yes no answers but that in itself is a binary decision there is no in between. So we can easily translate binary and Boolean logic back and forth. Commonly speaking, one is going to mean true and zero is going to mean false. Now, this is the same thing is translated in a variety of other contexts, like electrical systems where a on or off signals being produced one or on meaning electrical current, or off or zero. meaning no electrical current. So while these are traditional representations in many electrical and programming contexts, these values can be reversed for a variety of reasons. And really the moral of the story here is make sure you know which one you're working on. 

