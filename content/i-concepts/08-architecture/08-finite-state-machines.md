---
title: "\u2705 \u2705 Finite State Machines"
pre: "8.8 "
weight: 35
date: 2020-08-28T16:27:26-05:00
---

{{< youtube X9LObTF_Fac >}}

<!-- CIS 115: XM4oHcFMzvQ -->

#### Resources
* [Slides](../slides/8-Computer_Architecture.pdf)

#### Video Script

So far, we've looked at the parts of a modern computer all the way from the integrated circuit to the CPU and RAM that we have in our modern computers. But we still haven't talked about how we can use those computers to represent real world systems and actually do something useful. To do that, we have to look at one more thing from computer science called the finite state machine. a finite state machine is a theoretical device that has a limited number of states. And those states can be changed based on the transitions that we get based on some inputs. 

For example, take a look at the finite state machine diagram on this slide. Do you recognize it? This diagram shows what we might see if we mirrored a door as a finite state machine. A door has two states open and closed and it has two transitions the closed door state which allows us to take an open door and make it closed and the open door state which takes a closed door and makes it opened So obviously, we can use finite state machines to represent all sorts of different real world ideas, like the ones on this slide. This slide lists a few different things that you might come in contact with during your daily lives. And all of these things can be represented using finite state machines if we think about them in just the right way. 

So let's go through an example of what it would take to create a finite state machine diagram for one of these devices. The one that I like to do is the one for a stoplight. So let's take a look at that. Imagine for example that we have a crossroads where two roads meet and there's a stoplight that helps control traffic that comes to this crossroad. We can represent a finite state machine of a stoplight by thinking about the states that are stoplight could have most stoplights we know today have three states, a red states, a green state and a yellow state. So a modern stoplight will start at the red state and then it will go to the green states. Then after a certain time, it will go to yellow. And then finally, it will go back to red. That's a pretty simple finite state machine, but it does help explain exactly how a stop light works. Of course, this is just for a single stoplight. at a crossroads like what shown here, we probably actually have two stoplights that are working in tandem to control both directions. So that might be represented by a few more states. 

For example, let's say both stoplight start out initially as red. Then one stoplight switches to green and allows traffic to pass in that direction. After a certain amount of time that stoplight will go to yellow, and then we will go back to red red. However, notice that this state is different than the previous red red state because now we're going to go to green red Then of course, we go to yellow red. And finally, this state will go back to red, red. So now we've gone from three states to six states to represent a two direction stoplight. 

But of course, there's more to it than that. For example, let's say that this green light would be on the main highway, we don't want to always interrupt that traffic flow if there's nobody waiting. So we might have another state here, that is a wait state, we get to red green. And then we wait until we get some sort of sensor input saying there's a car on the other road that needs to pass. Then we could switch to yellow and red, and then switch the other road to green for a little bit to allow that car to pass. And of course, we could also have stoplight states. And so for example, green, we might still need to have the stoplight, say walk and then flash. And then don't walk before we get to the yellow states. And then of course, we can have buttons for the stoplights. We can have buttons for the crosswalks, there could be a lot of different things going on here that are all different states that we have to model within our finite state machine. 

So as you can see, even a simple stoplight controller with two directions could have as many as 10 or 15 unique states that describe how it works. This is the real power of a finite state machine. It allows us to easily describe how real world devices work. And then we can build computer programs to represent the states and transitions of that device and run it on a computer simulation. So if you want to follow along, see if you can do one of these or two of these as an example by creating a finite state machine diagram yourself. I think you'll find it to be a very valuable exercise and understanding exactly how a finite state machine works.