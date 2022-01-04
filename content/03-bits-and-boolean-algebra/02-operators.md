---
title: "Operators"
pre: "3.2 "
weight: 10
date: 2020-05-27T10:53:26-05:00
---

{{< youtube L7ibGfyWNAU >}}


### Resources

* [Slides](/1-cc110/03-bits-and-boolean-algebra/slides/03-Bits-and-Boolean-Algebra.pdf)

### Video Script

#### Boolean Operators (Slide 6)

##### And
Let's take a look at what the Boolean and operator does out in this Venn diagram here we're going to kind of use these to showcase where the Boolean statements that we're checking out with the Boolean operator where these statements are actually evaluated to be true. So if we assume that we are two facts here, A and B are both true. So let's say this inner circle here, this left circle here represents a and this right circle here represents B and the square on the outside represents everything else. So when a and b are not, so if A and B are both true, then the statement evaluates to true. So the left hand side and the right hand side of the operator both must be true in order for the whole statement to be true. If A is false, or B is true. false, then the whole thing would be false. Now if we introduce a third fact, see, we kind of get the same results, right. So similar kind of story with the Venn diagram. Here we have a, b, and c. But notice that this little square here where we were actually filled in over here is no longer filled in. And that's because all three facts must be true for the whole statement to evaluate to true. So a has to be true, B has to be true. And C has to be true in order for the whole statement to evaluate true. 

##### Or

So we'll have similar representation here for the OR operator where the English word is the representation in Python of the OR operator the double bar symbol, so this is just the two vertical bars from your keyboard that is the OR operator in Java, C sharp and other programming languages and then a capital V is great. To be the OR operator for Boolean algebra. So let's take a look at how or operates. So if we have the same statement, as we have before the same two premises A and B both being true initially, and the circles are kind of the representation of the same thing here, but the OR operator will evaluate to be true if either side of the operator are true. So if the left hand side is true, or the right hand side is true, the whole thing will be true. So if A is true, or B is true, so left hand side and the right hand side, so if A or B is true, then the whole statement is also true. And so nothing on the outside will actually be filled in quite yet. And the similar kind of story is for a third fact or fifth, that one has to be true for the whole statement to be true. So if any of them are true, the whole thing is true, but things kind of get tricky when we're in introduce this next operator the exclusive OR exclusive or you won't really find normally in programming languages. The Exclusive OR can be simulated using and or and the next operator that we'll be covering here in just a second. 

##### XOr

But the exclusive OR works in a little bit of a different way than the regular or the exclusive OR operates very similar to what we would expect the normal or operator to be in the sense that if A is true, or B is true, the statement is true, but notice that a and b is now false. If a and b are both true, the statement is false. So the exclusive OR operator is expecting one or the other. So that means the left side or the right side must be true, but not both. That is where the exclusive portion of the exclusive OR or the X or operator actually comes out. If I introduce a third fact things get to be a little bit more difficult to understand because now I would expect it to be kind of similar pattern as we have up here just to be, or on my just with my two facts, everything in the middle would be white, but everything on the outside would be red. But you notice when when we have all three to be true, all three can be true and the exclusive OR would still be true. Now let's take a look at why that would be the case. 

##### XOr White Board Example

So let's take a look at the example that we saw on the slides. We have our facts a, and our XOR operator. So we have a XOR B XOR. See, now if we kind of do our substitutions here now we could substitute ones and zeros here are true and false. So let's go ahead and substitute our Boolean values here for our variables. So if A is true So we have a XOR B, which is also true. And C, which is also true. Now, just like most of your math problems, even when you're just doing multiplication and division, you're always going to evaluate your statement from the left to the right. So we need to first evaluates true x or true now XOR Exclusive OR exclusive right, the left or the right can be true, but not both. Since the left hand side of my operation is true, and the right hand side of my operator is true, this portion of the statement evaluates to false. Then all we need to do then is keep on working the rest of our statements. So we still have one XOR left. So we have false x or true? Now exclusive or one side or the other must be true but not both. So false x or true is actually true because both sides aren't true. So this statement you say a false x or true, evaluates to true. So the whole thing true x our true, false XOR true, ends up being true. 

##### Not (Slide 6)

So our last Boolean operator here is the NOT operator. The NOT operator acts pretty much like negation, as you would expect, like multiplying something by negative one not something is the opposite of what it actually is in Python as the previous Boolean operators the and and the OR operator, the NOT operator in Python is very English light not but Python is kind of weird. You will also see the exclamation point In some operations, but it doesn't mean the traditional knots or negation operator as in many other programming languages. So, again, you'll see not in Python, the exclamation point, this is going to be things like Java. And the weird sideways l here, this is going to be your Boolean algebra. So let's take a look at what the Boolean operator not actually looks like. As I mentioned, the NOT operator is a negation, so not something as the opposite. So not a or not true is false. So not a if I write a here, so everything in the circle is a so when A is actually true, so everything inside of the circle then everything on the outside of a is actually true because it's negated and similar idea for B when B is true, everything But B is true. So the whole statement is evaluated as such and similar idea if I introduce a third fact. So if I have three facts A, B and C, not B means that everything but B is true, just like in this example here. 
