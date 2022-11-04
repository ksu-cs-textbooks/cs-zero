---
title: "AP Syllabus"
pre: "1. "
weight: 10
---

## Big Ideas Guide

* **CRD** - Creative Development
* **DAT** - Data
* **AAP** - Algorithms & Programming
* **CSN** - Computer Systems & Networks
* **IOC** - Impact of Computing

Reference: [AP Course and Exam Description](https://apcentral.collegeboard.org/media/pdf/ap-computer-science-principles-course-and-exam-description.pdf)

## CR 1 - Resources

_The teacher and students have access to college-level computer science resources, in print or electronic format._

The primary teaching resource in this course is _Introduction to Computing_, an eTextbook authored by K-State faculty. The textbook consists of lecture material and videos developed and presented by K-State faculty, as well as an annotated bibliography of additional readings and videos from across the internet on each topic. The textbook is used in two college-level courses taught at K-State:

* CIS 115 - Introduction to Computing Science
* CC 110 - Introduction to Computing

The textbook can be found online at:

* Primary Link: https://textbooks.cs.ksu.edu/cc110/
* Alternate Link: https://ksu-cs-textbooks.github.io/cszero/ 
* Authors & Contributors: https://core.cs.ksu.edu/authors/

Much of the content in the eTextbook is broadly inspired by two books:

* _The Pattern on the Stone: The Simple Ideas That Make Computers Work_ by W. Daniel Hillis
* _Nine Algorithms That Changed the Future: The Ingenious Ideas That Drive Today's Computers_ by John MacCormick

These books are recommended reading for students in the AP version of this course but are not required. 

## CR 2 - Develop Understanding of Content

_The course provides opportunities to develop student understanding of the required content outlined in each of the big ideas described in the AP Course and Exam Description._

The course consists of two major types of content:

* Lecture Content, Videos, Discussions, Activities & Quizzes - roughly 2 college credit hours
* Programming Content, Labs, and Homeworks - roughly 1 college credit hour

They are separated to allow teachers flexibility in structuring the course each semester. Below is an outline of the modules in each content area.

### Lecture Content

#### Unit 1 - CS Concepts

##### Chapter 1 - What is Computing Science?

Students are introduced to the field of computer science, including the original definition of a computer. They will learn about the reasons why pioneers such as Babbage and Lovelace desired to build machines to handle computations, reducing the risk of human error when computing mathematical tables. 

* **DAT** 3.2 Data Abstraction, 3.16 Simulations
* **IOC** 5.1 Beneficial & Harmful Effects

Notes: Add direct call-out to simulation, talk about beneficial effects of computing

##### Chapter 2 - Early Computing Machines

Students learn about the early history of computing machines, including the Antikythera Mechanism, abacus, and slide rule. Students then discuss and explore what features must be present in a device in order for it to be considered a computer, aiming for computation, storage, input, and output. Students are then introduced to key devices that pioneered the development of these features, such as Pascal's Calculator and the Leibniz Wheel (computation), Jacquard Loom (input via punch cards), Babbage's Difference Engine (output via press plates), and Babbage's Analytical Engine (integrating all items and including a storage mechanism). Students will see that the development of computer technology required input from many areas.

* **CRD** 1.1 Collaboration, 1.2 Program Function & Purpose

Notes: clearly call out the collaboration needed to build these tools; discuss how they were built to solve specific problems and have a set purpose

##### Chapter 3 - Bits & Boolean Algebra

Students are introduced to the concepts in Boolean logic, including the AND, OR, NOT, and XOR operators. Students then explore Boolean algebra, observing how many of the rules have parallels directly to mathematics. Students also explore DeMorgan's Theorem. Students work on several examples in class, going from truth tables to Venn diagrams and finally Boolean logic expressions. From there, students see how Boolean logic can be implemented using simple electronic circuits, forming the building blocks of modern computers.

* **AAP** 3.5 Boolean Expressions

Notes: add discussion and examples to teacher guide

##### Chapter 4 - Programming

Students explore the history of programming and many diverse pioneers such as Grace Hopper, Ada Lovelace and Margaret Hamilton. Students then learn what it means to actually "program" a computer and explore the process of taking code written in a high-level language (such as Java) and using tools such as compilers, interpreters, and assemblers to convert that code to assembly and eventually machine-level instructions that can actually be performed by a computer. 

* **CRD** 1.1 Collaboration, 1.2 Program Function & Purpose
* **AAP** 3.2 Data Abstraction

Notes: show how modern programming process is built upon the work of many pioneers; discuss how high-level code and machine code demonstrate abstraction

##### Chapter 5 - Universal Computers

Students learn about the work of Alan Turing and the concepts behind a universal computer like the Turing Machine. Students work through an example to build a simple Turing machine to mimic Boolean logic operators using a few simple instructions. From there, students see how the concept of a universal computer, coupled with the prior concepts from other historical computers, led to the creation of the Von Neumann Architecture that is used in most modern computers. 

* **CRD** 1.1 Collaboration
* **AAP** 3.2 Data Abstraction, 3.9 Developing Algorithms, 3.16 Simulations

Notes: add Turing machine examples to teacher guide; clearly address turing machines as simulations. Add decidability?

##### Chapter 6 - Algorithms

Students learn about Al-Khwarizmi and the history of the word "algorithm" before exploring simple algorithms such as Euclid's Algorithm. Students then go through an activity using playing cards to learn about four different sorting algorithms - insertion/selection sort, bubble sort, merge sort, and quicksort. At each step, students discuss how many "steps" it took to complete the algorithm, and then use that data to explore algorithmic complexity. Students are then introduced to Big-O notation as a way to compare the running time of algorithms, and by analyzing quicksort they also learn about the difference between worst-case and expected-case performance. Students are then introduced to the Traveling Salesman problem as a way to explore heuristics and the development of faster algorithms to find a good answer, but not necessarily the best answer. 

* **AAP** 3.9 Developing Algorithms, 3.17 Algorithmic Efficiency

Notes: add binary search? discuss lists? 

##### Chapter 7 - Encoding

Students learn about the work of George Stibitz and the creation of the Model K computer, one of the first to use binary values when performing calculations. Using that motivation, students learn about binary numbers and representation, including twos complement for negative values, floating-point for decimal values, ASCII for text, and both vector and raster image formats. Students also briefly see the basics of compression by replacing repeated data with smaller representations, but also see a case study showing how that can lead to loss of data and errors if done improperly.

* **DAT** 2.1 Binary Numbers, 2.2 Data Compression, 2.3 Extracting Information from Data
* **AAP** 3.2 Data Abstraction

Notes: add examples to do in class

##### Chapter 8 - Computer Architecture

Students learn about the development of the integrated circuit, seeing how it was the culmination of many small advancements by many different groups and how it helped solve the "Tyranny of Numbers" complexity problem of computers at that time. From there, students learn about Moore's Law and how more and more components are placed on integrated circuit chips, leading to the first microprocessor in the Intel 4004 chip. Students also are re-introduced to Von Neumann Architecture and the parts of a modern computer. Finally, students perform an in-class exercise introducing finite state machines and how they can be used to represent real-world ideas in a computer program.

* **CRD** 1.1 Collaboration
* **AAP** 3.3 Data Abstraction, 3.9 Developing Algorithms, 3.16 Simulations

Notes: add finite state machine examples, talk about simulations

##### Chapter 9 - Software Engineering

Students learn about the practice of software engineering, including the software crisis and the recognition of the need for better language structures and processes. Students explore the various stages of the software development life cycle and different methodologies such as waterfall, iterative/incremental development, and agile.

* **CRD** 1.1 Collaboration, 1.3 Program Design & Development
* **IOC** 5.1 Beneficial & Harmful Effects

Notes: Add more on impacts? Take information from CIS 400/CC 410? In-class activity?

##### Chapter 10 - Human-Computer Interaction

Students are introduced to the field of human-computer interaction, starting with the work of Douglas Engelbart and the "Mother of all Demos" exploring his NLS system. Students then learn about the history of modern computer interfaces, including the creation of the desktop metaphor used in most modern systems. Students also learn about some failed experiments such as Microsoft Bob and discuss what makes a good or bad interface. Students see the work of Don Norman and user-centered design. Finally, students are introduced to several new and interesting concepts in HCI and future computer interfaces, such as virtual/augmented reality, multi-touch interfaces, and examples of building accessible interfaces. 

* **CRD** 1.2 Program Function & Purpose
* **IOC** 5.1 Beneficial & Harmful Effects, 5.4 Crowdsourcing

Notes: discussion guide for Mother of All Demos? 

#### Unit 2 - The Internet

##### Chapter 11 - The History of the Internet

Students explore the history of the internet, starting with J.C.R. Licklider and his "Intergalactic Computer Network" concept, leading to the creation of the ARPANET. Students see videos and information from many pivotal figures in the history of the internet including Leonard Kleinrock, Vint Cerf, and Tim Berners-Lee. Students learn how the development of HTML and the world wide web helped bring the internet to the public, and how the dot-com bubble was a major turning point in the early internet before the rise of social media. 

* **CRD** 1.1 Collaboration 
* **CSN** 4.1 The Internet
* **IOC** 5.1 Beneficial & Harmful Effects, 5.4 Crowdsourcing

##### Chapter 12 - How the Internet Works

Students learn about the developments that lead to the technology behind the internet, such as packet-switching, and the various protocols that make up the seven layer OSI network model. Students learn how these developments were meant to build robust, fault-tolerant networks that can work in a variety of conditions.

* **CSN** 4.1 The Internet, 4.2 Fault Tolerance

##### Chapter 13 - Web Programming

Students learn the basics of web programming including HTML and CSS, and build a simple JavaScript Tic-Tac-Toe game to explore interactivity on webpages. 

* **CRD** 1.3 Program Design & Development
* **AAP** 3.12 Calling Procedures, 3.13 Developing Procedures
* **CSN** 4.1 The Internet

#### Unit 3 - CS Topics

##### Chapter 14 - High Performance Computing

Students learn about the concepts behind high-performance computing and why we need larger and more powerful computers to tackle some of the world's biggest problems. Students explore ways that large problems can be broken down into smaller parts and run in parallel on multiple computers. Students also see some real-world examples of problems that high-performance computing can solve. Finally, students are given a virtual tour through K-State's own supercomputer. 

* **CRD** 1.1 Collaboration, 1.3 Program Design & Development
* **Data** 2.4 Using Programs with Data
* **CSN** 4.3 Parallel & Distributed Computing
* **IOC** 5.1 Beneficial & Harmful Effects

##### Chapter 15 - Compression & Error Checking

Students explore various ways that data can be compressed, including run-length encoding and Huffman coding. Students also learn about methods for detecting and correcting errors in data, such as checksums. 

* **DAT** 2.2 Data Compression, 2.3 Extracting Information from Data
* **AAP** 3.2 Data Abstraction, 3.9 Developing Algorithms
* **CSN** 4.2 Fault Tolerance

##### Chapter 16 - Cryptography

Students learn the fundamental concepts and history of cryptography, starting with simple substitution ciphers. Students follow a case-study of the enigma machine and how it was defeated by the work of Alan Turing and others during the second world war. Students learn about modern cryptography principles including public-key cryptography, digital signatures, and perform a simple example of RSA encryption. 

* **CSN** 4.1 The Internet
* **IOC** 5.1 Beneficial & Harmful Effects, 5.4 Crowdsourcing

Notes: Add discussions!

##### Chapter 17 - Cybersecurity

Students explore the basics of cybersecurity, including a math-based discussion of passwords and relative password strength, as well as how passwords can be stored securely in a program. Students also learn about various cybersecurity threats such as social engineering. 

* **CSN** 4.1 The Internet
* **IOC** 5.1 Beneficial & Harmful Effects, 5.5 Legal & Ethical Concerns, 5.6 Safe Computing

Notes: Add discussions!

##### Chapter 18 - Artificial Intelligence

Students explore the field of artificial intelligence and what it means to say a machine is intelligent. Students engage in a discussion around the Turing Test and the Chinese Room counterexample. Students learn about intelligent agents and how they are used throughout the world, and explore other AI advancements such as neural networks and deep learning. 

* **DAT** 2.3 Extracting Information from Data, 2.4 Using Programs with Data
* **AAP** 3.16 Simulations
* **IOC** 5.1 Beneficial & Harmful Effects, 5.3 Computing Bias

Notes: Add discussions!

##### Chapter 19 - Search & Information Retrieval

Students explore the basics of databases and relational data. Students also learn about how information can be indexed and searched, followed by an introduction to ranking and the process of page rank for web searches. 

* **DAT** 2.3 Extracting Information from Data, 2.4 Using Programs with Data
* **AAP** 3.9 Developing Algorithms, 3.16 Simulations
* **CSN** 4.1 The Internet
* **IOC** 5.1 Beneficial & Harmful Effects, 5.3 Computing Bias, 5.4 Crowdsourcing

Notes - add bias to discussions

##### Chapter 20 - Big Data

Students explore the impact of big data in computing and how it is being used to solve large-scale real-world problems in areas such as healthcare. Students are also introduced to the concept of map-reduce in programming.

* **DAT** 2.3 Extracting Information from Data, 2.4 Using Programs with Data
* **AAP** 3.9 Developing Algorithms
* **CSN** 4.3 Parallel & Distributed Computing
* **IOC** 5.1 Beneficial & Harmful Effects, 5.4 Crowdsourcing

##### Chapter 21 - Ethics

Students explore some of the legal and ethical impacts of computing, including intellectual property, bias, privacy, and fair use. Students also learn about the digital divide and how that impacts access to information and equity. 

* **IOC** 5.1 Beneficial & Harmful Effects, 5.2 Digital Divide, 5.3 Computing Bias, 5.4 Crowdsourcing, 5.5 Legal & Ethical Concerns

Notes - this is pretty aspirational?

##### Chapter 22 - Graphics & Video Games

Students explore the basics of computer graphics and how they have evolved over time. Students learn about the "uncanny valley" effect. Students also see how early video game graphics were built, exploring concepts related to data compression and efficiency on such small systems.

* **DAT** 2.1 Binary Numbers, 2.2 Data Compression
* **AAP** 3.16 Simulations, 3.17 Algorithmic Efficiency

### Programming Content

#### Lab 1 - Introduction

This lab introduces students to the basics of the Codio interface and gives some examples of the various assessments contained in the labs.

#### Labs 2 & 3 - Basic Programming

These labs introduce students to the basic syntax of both pseudocode and Python. Students learn how to use a simple Linux terminal to navigate the file system and execute programs. Students learn to use `print` to display output, and explore examples of printing input with and without newline characters. Students learn to create basic variables that store strings. Students explore code tracing both by hand (in pseudocode) and using Python Tutor. Finally, students learn to create functions or procedures, including simple parameters and arguments, and learn how to create a `main` function or procedure for their programs. 

* **CRD** - 1.2 Program Function & Purpose, 1.3 Program Design & Development, 1.4 Identifying & Correcting Errors
* **AAP** - 3.1 Variables & Assignments, 3.2 Data Abstraction, 3.4 Strings, 3.12 Calling Procedures, 3.13 Developing Procedures

#### Labs 4 & 5 - Operations & Input

These labs introduce math and string operators in both pseudocode and Python. Students learn about integer and floating-point data types and how to convert between the two. In addition, students learn how to return data from functions or procedures, and explore how to use the basics of function composition to combine expressions into more complex statements, such as using the result of a function call directly as an argument to another function. Students learn how to request input from the user and convert a string into a numerical value. 

* **CRD** - 1.2 Program Function & Purpose, 1.3 Program Design & Development, 1.4 Identifying & Correcting Errors
* **DAT** - 2.1 Binary Numbers, 2.4 Using Programs with Data
* **AAP** - 3.1 Variables & Assignments, 3.3 Mathematical Expressions, 3.12 Calling Procedures, 3.13 Developing Procedures

#### Labs 6 & 7 - Conditionals

These labs introduce students to conditional statements in both pseudocode and Python. Students learn about the Boolean data type and a number of Boolean operators and comparators used in Boolean expressions. Students then learn about if and if-else statements, and explore how to test their programs by developing inputs that achieve branch and path coverage. 

* **CRD** - 1.2 Program Function & Purpose, 1.3 Program Design & Development, 1.4 Identifying & Correcting Errors
* **AAP** - 3.1 Variables & Assignments, 3.3 Mathematical Expressions, 3.5 Boolean Expressions, 3.6 Conditionals, 3.9 Developing Algorithms, 3.12 Calling Procedures, 3.13 Developing Procedures

#### Lab 8 - Homework 3

This lab is a stand-in for homework 3, which is partially done in-class along with the unit on web programming. It is discussed below. 

#### Lab 9 - Nested Conditionals

In this lab, students explore the concepts being nesting and chaining conditionals. Students learn about the usefulness of mutual exclusion when designing conditional statements, and also explore the concept of variable scope and blocks of code. 

* **CRD** - 1.2 Program Function & Purpose, 1.3 Program Design & Development, 1.4 Identifying & Correcting Errors
* **AAP** - 3.5 Boolean Expressions, 3.6 Conditionals, 3.7 Nested Conditionals, 3.9 Developing Algorithms, 3.12 Calling Procedures, 3.13 Developing Procedures

#### Labs 10 & 11 - Loops

This lab introduces the concepts of loops and iteration in both pseudocode and Python. Students will see both for loops (iterating across a collection or range) and while loops (iterating while a Boolean condition is true). Students also learn how to use loops to prompt for input and repeat until a valid input is received. Students learn to test loops using inputs that achieve branch and path coverage. Students also learn how to import the `random` library in Python and generate random integer values in a range. 

* **CRD** - 1.2 Program Function & Purpose, 1.3 Program Design & Development, 1.4 Identifying & Correcting Errors
* **AAP** - 3.5 Boolean Expressions, 3.8 Iteration, 3.9 Developing Algorithms, 3.12 Calling Procedures, 3.13 Developing Procedures, 3.14 Libraries, 3.15 Random Values

#### Lab 12 - Nested Loops

This lab reinforces previous learning on loops with examples on how to nest a loop inside of another loop. Students will learn how skills for tracing execution through these loops by hand and using Python tutor. Students also learn skills for testing these loops and developing inputs that properly explore the edge cases. 

* **CRD** - 1.2 Program Function & Purpose, 1.3 Program Design & Development, 1.4 Identifying & Correcting Errors
* **AAP** - 3.5 Boolean Expressions, 3.8 Iteration, 3.9 Developing Algorithms, 3.12 Calling Procedures, 3.13 Developing Procedures

#### Lab 13 - Lists

This lab introduces students to the list data structure in Python. Students learn about the list data type, including accessing elements by index and adding elements. Students explore how to use loops with lists to iterate through elements. Students learn that lists are handled in a "pass by reference" way when used as arguments to functions. Students learn that strings can also be treated like lists, and that lists can be sliced in a variety of ways.

* **CRD** - 1.2 Program Function & Purpose, 1.3 Program Design & Development, 1.4 Identifying & Correcting Errors
* **DAT** - 2.4 Using Programs with Data
* **AAP** - 3.1 Variables & Assignments, 3.2 Data Abstraction, 3.4 Strings, 3.9 Developing Algorithms, 3.10 Lists, 3.12 Calling Procedures, 3.13 Developing Procedures 

#### Lab 14 - Dictionaries

This lab introduces the dictionary data structure in Python. Students learn how to add and access elements in a dictionary, and how to iterate through all elements in a dictionary, including both keys and values. Students also see that dictionaries are treated similar to lists when used as function arguments. 

* **CRD** - 1.2 Program Function & Purpose, 1.3 Program Design & Development, 1.4 Identifying & Correcting Errors
* **DAT** - 2.4 Using Programs with Data
* **AAP** - 3.1 Variables & Assignments, 3.2 Data Abstraction, 3.4 Strings, 3.9 Developing Algorithms, 3.10 Lists, 3.12 Calling Procedures, 3.13 Developing Procedures, 3.16 Simulations

#### Homework 1

The first homework typically involves some sort of mathematical simulation, such as compound interest. It reinforces the topics of variables, numeric and string data types, reading input, using math operators, and formatting output. 

* **CRD** - 1.2 Program Function & Purpose, 1.3 Program Design & Development, 1.4 Identifying & Correcting Errors
* **AAP** - 3.1 Variables & Assignments, 3.2 Data Abstraction, 3.3 Mathematical Expressions, 3.4 Strings, 3.5 Boolean Expressions, 3.9 Developing Algorithms, 3.12 Calling Procedures, 3.13 Developing Procedures, 3.16 Simulations

#### Homework 2

The second homework typically involves conditional statements as well as mathematical operators and more practice with input, output, and functions.

* **CRD** - 1.2 Program Function & Purpose, 1.3 Program Design & Development, 1.4 Identifying & Correcting Errors
* **AAP** - 3.1 Variables & Assignments, 3.3 Mathematical Expressions, 3.5 Boolean Expressions, 3.6 Conditionals, 3.9 Developing Algorithms, 3.12 Calling Procedures, 3.13 Developing Procedures, 3.16 Simulations

#### Homework 3 

The third homework introduces students to creating websites with HTML and CSS. Students also follow a tutorial to create a simple game in JavaScript to explore interactivity on web pages. 

* **AAP** - 3.2 Data Abstraction, 3.14 Libraries
* **CSN** - 4.1 The Internet

#### Homework 4

The fourth homework covers the use of nested conditional statements, as well as user input and handling functions with parameters and return values.

* **CRD** - 1.2 Program Function & Purpose, 1.3 Program Design & Development, 1.4 Identifying & Correcting Errors
* **DAT** - 2.3 Extracting Information from Data, 2.4 Using Programs with Data
* **AAP** - 3.1 Variables & Assignments, 3.2 Data Abstraction, 3.3 Mathematical Expressions, 3.4 Strings, 3.5 Boolean Expressions, 3.6 Conditionals, 3.7 Nested Conditionals, 3.9 Developing Algorithms, 3.12 Calling Procedures, 3.13 Developing Procedures, 3.16 Simulations

#### Homework 5 

The fifth homework covers the use of loops and advanced data structures such as lists or dictionaries. It usually involves a larger amount of input, either a string or a list of values. 

* **CRD** - 1.2 Program Function & Purpose, 1.3 Program Design & Development, 1.4 Identifying & Correcting Errors
* **DAT** - 2.3 Extracting Information from Data, 2.4 Using Programs with Data
* **AAP** - 3.1 Variables & Assignments, 3.2 Data Abstraction, 3.3 Mathematical Expressions, 3.4 Strings, 3.5 Boolean Expressions, 3.6 Conditionals, 3.7 Nested Conditionals, 3.8 Iteration, 3.9 Developing Algorithms, 3.10 Lists, 3.12 Calling Procedures, 3.13 Developing Procedures, 3.16 Simulations

## CR 3 - Develop Understanding of Big Ideas

_The course provides opportunities to develop student understanding of the big ideas._

## CR 4 - CT Practice 1: Computational Solution Design

_The course provides opportunities for students to develop the skills related to Computational Thinking Practice 1: Computational Solution Design, as outlined in the AP Course and Exam Description._

## CR 5 - CT Practice 2: Algorithms & Program Development

_The course provides opportunities for students to develop the skills related to Computational Thinking Practice 2: Algorithms and Program Development, as outlined in the AP Course and Exam Description._

## CR 6 - CT Practice 3: Abstraction in Program Development

_The course provides opportunities for students to develop the skills related to Computational Thinking Practice 3: Abstraction in Program Development, as outlined in the AP Course and Exam Description._

## CR 7 - CT Practice 4: Code Analysis

_The course provides opportunities for students to develop the skills related to Computational Thinking Practice 4: Code Analysis, as outlined in the AP Course and Exam Description._

## CR 8 - CT Practice 5: Computing Innovations

_The course provides opportunities for students to develop the skills related to Computational Thinking Practice 5: Computing Innovations, as outlined in the AP Course and Exam Description._

## CR 9 - CT Practice 6: Responsible Computing

_The course provides opportunities for students to develop the skills related to Computational Thinking Practice 6: Responsible Computing, as outlined in the AP Course and Exam Description._

## CR 10 - Investigate Computing Innovations

_The course provides a minimum of three opportunities for students to investigate different computing innovations._

## CR 11 - Create Performance Task

_Students are provided at least 12 hours of dedicated class time to complete the AP Create Performance Task._