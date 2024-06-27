---
title: "Boolean Algebra"
pre: "3.3 "
weight: 13
date: 2020-05-27T10:53:26-05:00
---

{{< youtube nc7OgG3BYe4 >}}


#### Resources

* [Slides](slides/03-Bits-and-Boolean-Algebra.pdf)

#### Video Script

##### DeMorgan's Theorem (Slide 7)

So with all these new tools, we needed some new algebraic rules to really deal with them. Thankfully, most of the rules you know, apply quite well, but there's one rule that needed to be added. In mathematics. When you multiply by negative one, you have to change the signs. Similarly, Augustus DeMorgan came up with a way to deal with the negation of entire Boolean logic statements. So this becomes very similar to how you multiply a statement or a regular mathematical statement by a negative one. I guess system marking came up with a way to deal with the negation of entire Boolean logic statements.  The DeMorgan's theorem essentially states to treat the NOT operator like the negative sign so you're going to apply the negative to each of the premises or facts and then swap the operators or basically and become or's and or's become hands. So let's take a look at an example. So if we invert our particular statement here where we have a and b, right, so A and B, not a and b becomes not a or not B, so we negated or applied the knot to a and the knots to b and the knot and becomes or similar idea for or not a or b becomes not a, and not B. 

##### Boolean Algebra(Slide 8)

Now, in Boolean algebra, just like when you multiply by a negative one, a lot of the similar rules apply and Boolean algebra just like they do in mathematics. So in general, the OR operator works very much like the plus operator not works very much like negation, like we've already seen, and works very much like multiplication. 

The associative property, also Hold. So we have a and b, and c becomes a and b and c. So if I made the substitutions here, just based off of what we had here, if we had one, and the AND operator works like multiplication, though times two, parentheses, substitute the multiplication symbol and for the end, and then we have three. That is the same thing as saying one times two times three. 

The commutative property also holds. So again, let's try to make some substitutions. A and B is the same thing as saying B and A. So that's the same thing as saying. Two times three is the same thing as Three times two. 

And the distributive property also holds. So A and B or C is the same thing as saying a and b, or a and c. So let's make our substitutions again, let's substitute again, one four a, so one times to remember, or is like the addition operator plus three is the same thing as saying, we're going to kind of distribute right as we normally would with math, distribute the one across two plus three. So one times two plus three is the same thing as saying one times two, plus one times three. So we distributed the Want across and we'll end up with the same exact result. Same idea or Boolean logic if we make each one of these properties, as we seen here, and mathematics applies and works directly with Boolean algebra. So what this really helps you as when you start working with Boolean logic, even when programming you can actually use these properties to simplify a lot of your Boolean logic statements to make them easier to read and easier to program. 