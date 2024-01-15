---
title: "Heuristics"
pre: "6.10 "
weight: 45
date: 2020-08-10T16:27:26-05:00
---

{{< youtube Gwb9ezHE6VM >}}

#### Resources

* [Slides](../slides/6-Algorithms.pdf)

#### Video Script

So far in this module, we've studied algorithms, and remember that an algorithm is a specific set of steps that we can use to solve a problem. However, what if we're faced with a problem that we can't solve? Either because it's impossible, or because we have so much data that we can't possibly find the one right answer using an algorithm. In that case, we would use something we call a heuristic. A heuristic is an experience based technique we can use to find a satisfactory solution to a problem, which may or may not be the absolute best solution to that problem. For example, if we have a particular person, and we'd like to know what their height is, we could actually get out a tape measure and measure it. Or we could use a heuristic and say, well, you're standing next to that door and you look like you're about six feet tall. That would be an experience based technique or a heuristic to estimate how tall someone is. We of course, use heuristics every day. For example, we use the rule of thumb when Trying to measure things. We can take educated guesses based on our previous experience, we can use our common sense and find answers that seem logical. We can try an answer and see if we can work backwards and prove that that is an answer to the question. Or we can even take our problem and try and do a simpler problem first and use that information to solve our larger problem. 

The whole idea of heuristics lies in this graph on trade offs. This graph is very common in business circles. For example, in a business, it's usually said that you can have fast good or cheap, pick two. So you can have things that are fast and good. You can have things that are fast and cheap. And you can have things that are good and cheap, but not necessarily fast. I usually like to apply this diagram to fast food. You can think about your favorite fast food restaurants and place them somewhere in this diagram. Are they fast and good, but not necessarily cheap? Are they fast and cheap, but maybe not the best food you've had? Or are they good and cheap, but sometimes it takes a little bit to get your food It's really interesting to think about this diagram and the different things that we interact with in the world. Algorithms usually lie on the scale of good, they find the one right answer. They may be fast. They may be cheap in terms of memory or processor usage, but they generally will find the one right answer. For heuristics, we're looking closer to the fast and cheap side of this diagram, we can find an answer that is quick and we can find one that is very cheap to compute, but it may or may not be as good as the one right answer we could find using an algorithm. We just hope that it's good enough to be useful for our needs. 

Let's take a look at one common problem in computer science and see how we can apply a heuristic to solve this problem is called the Traveling Salesman Problem. The idea behind the Traveling Salesman Problem is that everyday a salesman has to set out from home and would like to visit all the towns on the map and make it home as soon as possible. And so here we have a very simple map that contains four towns and edges between the towns are the roads that are labeled with the distance between each town. So looking at this map, can we find a way that we can find a route between all four of these towns that is the shortest as possible. There are some algorithms that we can use to solve this problem. For example, we could use a brute force algorithm, we can just compute every possible path, which would be in the time of big O of n!. If you know what factorial is, you know that that's a very big number. For example, eight factorial would require 40,320 steps to solve this problem. It's a very, very, very large number. You using some advanced programming techniques, such as dynamic programming, we can cut this algorithm down to big O of 2^n, which is still a big number for eight cities that requires 256 steps, but it's not easy and it's not cheap to perform. However, there is this really cool heuristic that we can use. 

For the Traveling Salesman Problem. We can just pick any city as our City. In this example, we'll use B. And then we'll just go to the next closest city we haven't been to yet. And from that city will go to the next closest city from there. And we'll repeat this process until we visited all of the cities. So here's a graphic showing what the greedy solution might look like. We start at City B, and we noticed that City A is the closest city that we haven't been to, then from A, we can either go 42 miles to city C, or 35 miles to city D. So we'll go 35 miles to city D. And finally, from there, the only city we haven't been to a C, and so that will get us all of our diagram. So this solution requires 67 miles to complete the path is this the fastest way we could visit all four cities. As it turns out, there is a better solution to this. We'll look at that in just a minute. So this greedy algorithm runs in big O of (d*n) where d is the number of dimensions in the graph and ins the number of cities. So on a two dimensional graph with eight cities We would have 16 steps. That's much, much less than the 256 or 40,000 steps that we saw in an earlier example. Now, of course, the time that it takes to do this can vary widely based on how the data is presented and how it's sorted. But this is a pretty simple example. And actual optimal solution to this problem would require us to start at either city A or C,B,D. And of course, here we find an optimal solution of 62 miles. 

So why is the Traveling Salesman Problem so important in computer science? Well, let's consider one use of this problem, which is deliveries. For example, delivery companies, such as Amazon and UPS and FedEx and the United States Postal Service basically have to solve the Traveling Salesman Problem every single day. They have a set of locations that they need to visit, and they want to visit those locations in the most efficient way possible. And so these companies have invested lots of time and resources in computer systems that can help them solve this problem very efficiently. They come up with some very unique solutions. For example, there's some information online about how ups, for example, solves this problem such that its trucks don't have to make many left turns, because they found that the time they spent waiting at a turn before they can make a left turn is wasted. And so they try and build the routes in such a way that they're always making right turns so that it's very quick and efficient. So heuristics are just one example of ways that we can solve problems in computer science without using a particular algorithm that gets the right answer. Of course, heuristics are just another form of an algorithm. But the important thing to remember is with a heuristic we're trying to find a best answer that may not exactly be the most correct answer possible. But heuristics are at the core of a lot of what we do in computer science today, such as artificial intelligence and machine learning. All of the things that are related to that build upon this idea of heuristics, we're trying to find an answer that seems most likely, which may or may not be the actually correct answer that we're thinking of.