---
title: "Introduction"
pre: "9.1 "
weight: 5
date: 2020-08-28T16:27:26-05:00
---

{{< youtube s294o-N-iWo >}}

#### Resources
* [Slides](slides/9-SoftwareEngineering.pdf)

#### Video Script

<!-- TODO Fix Captions on Video and verify transcript - it is bad! -->

Welcome back everyone. In this video we're gonna be talking about software engineering. Now you should remember this particular machine the ENIAC, which was the first electronic computer in the United States. Programming the ENIAC was a really slow and laborious process though. To load a program, ENIAC's programmers Pictured here is Gloria Ruth Gordon, and, well, later Bolotsky, and Esther Gordon would physically rewire the hardware and a new configuration corresponding to the calculations indicated by the programmers. And so you can see them here moving actually the wires from different plug boards for the computer to actually make different calculations and operations work. So the task was made even more difficult by the secrecy involved with the machine. Initially, programmers weren't even able to see the schematics of the machine and had to pass their wiring instructions belong to the technicians. So the programmers didn't weren't even instructed on how the actual machine was built or how it worked. And they couldn't even actually run their program themselves. So you could imagine that that would be a really difficult task to actually accomplish writing successful programs for a computer that you didn't even know how it worked. 

But this was very similar to Alan Turing's original conception of the his famous Turing machine. And this machine had carried out hardwired instructions on data encoded as zeros and ones on an infinitely long paper tape. Turing had an epiphany with this machine, realizing that by making this machine read instructions on specific sequences of zeros and ones, as his machine booted, he could encode the program directly on the infinite tape with the data it was actually operating on. Now, this is a huge leap, because before right with this, we had a tyranny of numbers problem where the We're just getting so complex, that it became nearly impossible to make anything substantial in today's terms of software. 

But now that we can actually store the actual software alongside with the data actually being used the started to simplify the process. These ideas were incorporated into electronic computers by several computer scientists, including J. Presper Eckert and John Mauchly, inventors of the ENIAC computer, as well as John Von Neumann, who was the first to publish such an article about this architecture in this paper, the first draft of a report on The Ed vac. For this reason, a computer architecture allowing for stored programs is referred to as the Von Neumann architecture, and is the basis for modern digital computers. Stored programs also allowed us to develop bootstrap code or libraries of common procedures that can be reused for future programs. And we're loaded into the computer as it was warmed up. This is an important predecessor to modern programming libraries and operating systems. So as you can imagine a lot of these early computers, you ended up having to actually program basic operations anytime you actually wanted to work with something. So a lot of the software, a lot of things were done by hand, a lot of the things that we take for granted like user input, a lot of the mathematical operations that we use in modern programming languages, all of these libraries that we utilize to make our software a lot easier to write, and which allows them to be extremely functional and easy to read. And these weren't existing or at least didn't exist in a lot of the earlier software that was actually being developed. So our ability to store programs along with data and store programs, along with the actual system itself. Made a lot to future programs a lot easier and faster to write. 

But the next major invention in software design was the development of programming languages and the associated technologies of compilers and interpreters that allowed programmers to write programs and a higher level programming language that would then later be translated into machine language for a stored program computer. Pictured here is Grace Hopper, the creator of the first higher order programming language flow Matic and influential co creator of COBOL. A very popular or was very popular business programming language. The development of programming languages is especially important in that it allowed us to develop abstractions for simplifying development of software and allowing us to express significantly more complex ideas in computer code without a significant amount of more lines of information and code that had to be made with the software. 

But as programming languages diverse From their mathematical roots, and became more expressive, new challenges arose in making sure that programs were clear and easy to understand. This is further complicated by increasingly sophisticated nature of software that sought to accomplish more than earlier programs had ever had. Furthermore, the growing industry demand for software developers had led to often incompletely trained programmers entering the field. And so if you could even code a little bit, you probably could land a programming job. This is a pretty important turning point in the industry here because we had a rapid growth of actual technology. So not too long after world war two ended, electronic computers started to become smaller and more popular and they all of a sudden didn't take entire rooms to actually build right they weren't the size of school buses anymore, especially as we approached the personal computer era. 

We needed a lot more people to actually program there was a significantly higher demand for software and the demand for that software was even greater yet as far as the functionality would actually go for that particular software. So, as a result of all this sloppy programming, poorly understood designs and really the lack of systematic planning and execution, with these poorly trained programmers led to an era of our field being labeled as the software crisis. This spurred the development of a lot of different new technologies and approaches and approaches for developing software. 

Some of the key projects from this period include the IBM O's 360 project that ran drastically over budget while employing over 1000 programmers, and famously the fair act 25 radiation machines which would regularly display an error to their operators. So as a nurse would come in, and try to to administer a dose of radiation to let's say, a cancer patient, they would then try redoing the treatment because there was an error on the machine on on the screen or whatever. And they wouldn't realize that the machine had already delivered a dose of radiation, which led to a lot of patients actually dying or being crippled. 

Throughout the software crisis, a lot of important computer scientists made a lot of developments in contributions to software engineering, and one of the more important computer scientists of the day, like Edgar Dykstra and Nicolas Wirth sought to address these challenges through language design and better education for fledging budgeting computer scientists. This 1968 letter to the editor of the ACM journal by Dykstra underscores his concerns with the goto statement, which allowed for a very disjointed style of programming that would make programs difficult to debug and understand as the go to statement would allow you to jump back and forth between steps in your program without any concern for anything else. This and readability of and usability concerns as well as efficiency issues became one of the driving forces behind the evolution of programming languages. Where most currently use programming languages don't even have a go to statement like Python, and many of the many of the other popular languages that we use today. Other improvements included the addition of modules and information hiding, introduced by David Parnas concepts that eventually involve evolved into what we refer to now as the object oriented programming languages. 

In the same year, Margaret Hamilton, one of the NASA engineers responsible for simulating the Apollo missions on a computer. One of the most involved computer simulations attempted to that time, coined the term software engineering to describe the role she had played The stack of documents Next to her is actually one of the simulation results from that effort, which helps underscore just how large software projects were growing at that time. 
