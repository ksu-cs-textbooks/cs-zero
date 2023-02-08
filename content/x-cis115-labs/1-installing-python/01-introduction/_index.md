---
title: "Python on Windows"
pre: "1. "
weight: 10
date: 2021-01-15T00:00:01-05:00
---

{{< youtube U6uxnVMMZ98 >}}

<!-- TODO Update Video to remove Atom -->

In this lab, we're going to cover various ways to install Python on your computer. First, we'll cover the basic way to install Python on a Windows system. To begin, open a web browser and go to python.org/downloads. Here you can find downloads for the latest version of Python for Windows as well as other operating systems. I'm going to click the button here to download the latest version of Python for Windows. 

Once the file is downloaded, I can double click it to open and run the installer. When we run the installer, there are a couple of options that we'll want to change. Notice by default, it will install Python into this complicated directory here, which can make it very hard to find. Also, it does not add Python to the path which we definitely want to do. So we'll check mark this checkbox and then we will customize the installation. We'll go ahead and check mark the boxes to install all of the optional features. When choosing advanced options, we can check mark the option to install for all users, which will place Python in the program files directory, making it much easier to find. We can click install and it will install very quickly. 

Once we've installed Python on our computer, we can verify that it works by loading it in PowerShell. On Windows, I'm just going to search for PowerShell in the start menu to find that program. Once PowerShell loads, we can run Python using the `python` command. Notice that this is different than most Linux and Mac systems where to run Python version three, we must run the command `python3`. On Windows with the most recent installer, we can simply use the `python` command followed by `--version` to see the current version of Python. If we type `python3`, it might load the Microsoft Store in prompting us to install an older version of Python. This can get a bit confusing, it's one of the problems with Python is the inconsistent usage of the `python` command to refer to Python version two, and Python version three. So if you follow this guide to install Python on your computer, just be aware that anytime you see the `python3` command in documentation or in the labs, you'll just need to use the `python` command instead, which will run Python version three. 

To make it easy to write Python files on Windows, you may also want to install a text editor that is specifically designed for writing code. One of the easiest to use is Atom which is a text editor provided from GitHub. So we'll download and install that as well. Once again, once we've downloaded Atom, we can double click the installer to install it. Once Atom is installed and open, you can close all of the open tabs to get a view that looks like this. 

To make it easy to program in Python, we're going to create a folder just for the Python work in this course. To do that, I'm going to click the add folders button right here. In Windows, we recommend creating a folder inside of your users home directory for all of your programming work. By default, it will open up the Documents List. But to get to your users folder, we're going to go to the C drive, then Users. Then we'll find our username. And then in here, we're going to create a new folder. And I'm going to name this `cis115` to match the class. And we'll select that folder as the folder to open in Atom. Now we see a view similar to this. 

From here, we can easily add a Python file by right clicking on the folder and creating a new file. I'm going to name this file hello.py. And then inside of that file, I can type print hello world as a simple Hello World program. Once I've written that program, I can go to the File menu and choose to save the file. I can also use Ctrl+S to Save the file. Once I've done that that file should now exist on my system in that folder. 

Once we've done this, we can run this file using Python by again opening PowerShell. In PowerShell, we need to navigate to where that is that folder is found. Notice that PowerShell already opens into our users folder. So all we should have to do is type `cd cis115` to open up that folder. Then we can type `python` and the name of the file that we just created to run it. There we go. That's all it takes to run a Python program on your Windows system. It should give you enough to get started in this class. As always if you have any questions please feel free to reach out to either of the instructors or any of our TAs and we'd be happy to assist you 

