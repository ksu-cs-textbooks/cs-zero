---
title: "Parts of a Computer"
pre: "8.7 "
weight: 30
date: 2020-08-28T16:27:26-05:00
---

{{< youtube -0qGcKTOXcU >}}

<!-- CIS 115: ck5jX5NSRxw -->

#### Resources
* [Slides](../slides/8-Computer_Architecture.pdf)

#### Video Script

Let's spend a little bit more time looking at modern computer hardware and talking about some of the things that are related to what we've already discussed in this lab. On our modern CPUs, one of the things we have to keep in mind is the instruction set architecture or ISA, that is built around the ISA determines how the CPU actually interprets the binary ones and zeros in the program code and turns that into instructions that it can follow to perform the calculations needed. One of the most common instruction set architectures is the x86 in ISA, a that was developed all the way back in the 1980s as part of the IBM compatible computers. And for about 20 or 30 years, almost every computer supported the x86 ISA or something very similar. In the mid 2000s, we had the development of 64 bit architectures such as x86, IA-64, and some other architecture sets, and so most modern computer processors today use some variant of a 64 bit operating system and a 64 bit ISA. 

There are of course, some other instruction set architectures that are built for various types. For example, most mobile phones and small devices such as Raspberry Pi's use the arm instruction set architecture, which is a very different is a very much focused on low power devices. Macintosh used to use power PC, and in fact, they've recently announced that they're planning on moving to the ARM-ISA very soon. And then of course, for smaller embedded systems there are things such as the MIPS-ISA, which is really good for small embedded chips and circuits. 

Of course, every modern computer also includes a motherboard. A motherboard is the main chip that connects all the other devices of the system together. This slide shows some of the other parts of a modern computer motherboard, such as the CPU socket, memory slots, the northbridge and southbridge chips also today, just known as the chipsets. The on board graphics processor and sound card and some of the expansion slots where you can plug in things such as your larger graphics card or a sound card or anything else that you might have. Let's talk a bit more about the hardware you might find in a modern computer system. 

The first part we should talk about is the central processing unit or CPU. This is what actually does all of the computation and calculation on your computer and is basically the brains of the operation. CPUs have a lot of different features you can look at such as the architecture or instruction set architecture that they use, the clock speed, that they have, the number of cache memory chips that they use, and the number of processing cores that are available. And central processing units come in a variety of styles and a variety of costs. And they're all basically the brains of your computer. 

The next piece we can talk about is the memory usually referred to as the ram or random access memory. This is the memory that your computer uses to store the program it's running and the data that is currently operating on the ram can also vary based on the size and the speed at which you can access data. There's also different types and classes of memory. And they're even advanced features such as registered in ECC memory, which does error correction. 

Beyond that, you could also have the storage devices such as your hard drive or solid state drive. These are for more long term storage of data even while the computer is turned off. They can vary based on the capacity of the drive, the interface that it connects to your computer with, and even things such as the speed that it can read and write data. For some drives. We also worry about the latency or how long it takes to get that first piece of data off of the drive once we request it. There are also more advanced things you can do with your hard drives such as create a raid raids allow you to get better performance or better security by mixing multiple drives together. 

And there's so much more we could talk about CD drives or optical disk drives. We could talk about graphics cards, sound cards, wireless cards, network cards, all sorts of peripherals that go on your computer. So I think encourage you to take a look at the computer that you're using right now to watch this video and think about all the different parts that make up that computer and how they look in your system.