---
title: "Introduction"
pre: "12.1 "
weight: 5
date: 2020-08-28T16:27:26-05:00
---

{{< youtube Uj4nCnxKqyk >}}

<!-- CIS 115: gwdJX1NPI20 -->

#### Resources
* [Slides](/1-cc110/12-internettech/slides/11-How_the_Internet_Works.pdf)

#### Video Script

In this module, we're going to dive a little bit deeper into the technologies that allow the internet and the World Wide Web to work today. As we discussed in a previous video, early computer networks relied on circuit switching, where each computer had to have a direct connection to each other computer it needed to talk to. This was very cumbersome and very prone to error. And so we needed to come up with a better system for doing this. 

So a circuit switch network works a lot like a telephone network. If you want to call somebody in New York and you're in Los Angeles, there has to be solid wire connection between New York and Los Angeles from phone to phone to really enable that connection to work. But of course, with computers there is one major difference between how two computers communicate and how two humans communicate. Think about a phone call. When humans are on the phone, there's almost no downtime, either one person is speaking or the other person is speaking. With a computer network, however, the communication is much more interrupted computer will send a command. And it will have to wait for some time before it receives any data back. And likewise, the sending and receiving can be much, much faster. And so with packet switched networks, instead of needing a solid connection all the time, can we just take those little bursts of data and somehow transmit them as needed, leaving the other spaces open for other bits of data to come in as well. 

That's really what led to the idea of packet switch networks. And this is one of the big reasons that computers and phones really need different network architectures. And it was something we realized in the 1960s. So the work of building packet switching actually lies in the work of Paul Baran. Paul Baran was a researcher at the RAND Corporation in 1959. And he worked on building computer networks or any any type of network really, that would be reliable in the case of a nuclear attack. So for example, if we want to send a message across the United States and there's a nuclear attack somewhere in the middle, could we make sure that that message could get around the attack and still be received everywhere that it needed to be? Or more precisely, if networks went down? How could you actually get a communication across a network that was broken? So let's take a look at a video looking at the work of Paul Moran and his creation of packet switched networking and why it was so important.