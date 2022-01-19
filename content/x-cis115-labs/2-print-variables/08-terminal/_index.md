---
title: "Working in the Terminal"
pre: "8. "
weight: 80
date: 2021-01-15T00:00:01-05:00
---

{{< youtube H0ZDBdT1Opw >}}

#### Resources

* <a href="slides" target="_blank">Slides</a>

First, let's start with the basics of writing Python code in a file and running those files. This is the first major step toward actually writing a real program, but it can definitely be difficult the first time without prior experience to rely on. So, let's go through it step by step and make sure we know how to run our programs in Python.

At this point, we should already have Python installed on our system. For students using Codio, this is taken care of already. For students using their own computers, refer to an earlier lab to find instructions for installing Python on your system, or contact the instructors for assistance. 

To make sure that Python is installed and working, we'll need to open a terminal in our operating system. In Codio, this can be found by clicking the **Tools** menu at the top, and then choosing **Terminal**. More information can be found in the [Codio Documentation](https://docs.codio.com/develop/develop/ide/boxes/terminal.html). There may also already be one open for you if you are reading this content from within Codio. 

If you are working on your own computer, you'll need to open a terminal on your operating system. This should have been covered in the previous lab when you installed Python. On Windows, look for **Windows Terminal** or **Windows PowerShell** (not the old Command Prompt, which requires different commands). On Mac or Linux, look for an application called **Terminal**. Throughout this course, we'll call these windows the **terminal**, even though they may have slightly different names in each operating system.

Once we have the terminal open, we should see something like one of these examples:

![Linux Terminal](/cc110/images/lab3/terminal_linux.png)

![Windows Terminal](/cc110/images/lab3/terminal_win.png)

At this point, we should see a place with a blinking cursor, where we can type our commands. This is called the **command prompt** in the terminal. The first thing we can do is check to make sure Python is properly installed, and we can also confirm that it is the correct version. To do this, we'll enter the following command and press enter to execute it:

```bash
python3 --version
```

Hopefully, that command should produce some output that looks like this:

![Python Version](/cc110/images/lab3/python_version.png)

Here, we see that the currently installed Python version is 3.6.9. As long as your Python version number begins with a 3, you have correctly installed Python and are able to run it from the terminal. So, we can continue to the next part of this lab.

If you aren't able to run Python or aren't sure that you have the correct version, contact the instructor for assistance!

{{% notice note note-1 "Python 2 vs. Python 3" %}}

Notice that we have to use the command `python3`, including the version number, instead of the simpler `python` command here. This is because some systems may also have Python version 2, an outdated version of Python, installed alongside version 3. In that case, the simple `python` command will be Python version 2, while `python3` will be Python version 3. Unfortunately, most programs written in Python 3 will not run properly in Python 2, so it is important for us to make sure we are using the correct Python version when running our programs.

Thankfully, the command `python3` should always be Python version 3, and using that command is a good habit to learn. However, depending on how Python is installed on Windows, it might only work via the `python` command, which can make it confusing. So, throughout this course, we will use the command `python3` to run Python programs, but you may have to adapt to your particular situation. 

{{% /notice %}}

## Navigating in the Terminal

When we open a terminal, it will usually start in our user's home folder. This may mean different locations for different operating systems. For example, if our current user's name is `<username>`, the terminal will usually start in this location for each operating system:

* **Windows**: `C:\Users\<username>`
* **Linux**: `/home/<username>`
* **Mac**: `/Users/<username>`
* **Codio**: `/home/codio/workspace`

The directory that is open in the terminal is known as the **working directory**. We can use the `pwd` command to determine what our current directory is:

![Print Working Directory](/cc110/images/lab3/pwd.png)

In this example, we are looking at the Codio terminal, so our working directory is `/home/codio/workspace`. 

Next, we can see the files and directories contained in that directory using the `ls` command. Here's the output of running this command in Codio:

![List Directory Command](/cc110/images/lab3/ls.png)

In the output, we can see that there is a file named `README.txt` and a directory named `python`. In Codio, we'll place all of our files in the `python` directory, so we can open that using the `cd python` command:

![Change Directory Command](/cc110/images/lab3/cd.png)

Notice how the `python` directory is now included in the command prompt in the terminal. Most terminals will show the working directory in the command prompt in some way. 

That's the basics of navigating in the terminal, but there is much more to learn. If you'd like to know more, consider checking out some of the resources linked below!

### Resources

* [Basic Linux Navigation & File Management](https://www.digitalocean.com/community/tutorials/basic-linux-navigation-and-file-management) from DigitalOcean
* [Beginner's Guide to the Bash Terminal](https://www.youtube.com/watch?v=oxuRxtrO2Ag) by Joe Collins on YouTube

{{% notice note note-2 "Windows & Mac Terminal" %}}

Most of the content in this course will focus on using the commands that are present in the Linux terminal, since they are the most widely-used commands across all platforms. In general, these commands should work well on both Windows and Mac, with a few caveats:

* On Windows, there is an older Command Prompt tool that does not support the newer Linux commands. Therefore, we won't be using it. Instead, we only want to use **Windows PowerShell**, which supports most of the basic Linux commands via aliases to similar PowerShell commands. We can also install the [Windows Terminal](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701) application for a more modern interface.
* Windows users may also choose to install the [Windows Subsystem for Linux (WSL)](https://docs.microsoft.com/en-us/windows/wsl/about) to run Linux (such as Ubuntu) directly within Windows. Many developers choose to pursue this option, as it provides a clean and easy to use development environment that is compatible with the Linux operating system. 
* The Mac operating system includes a terminal that uses either ZSH (since OS X 10.15) or Bash (OS X 10.14 and below). This terminal is very similar to the Linux terminal when it comes to navigating the file system and executing programs, which is sufficient for this course.

Fully learning how to use these tools is outside of the scope of this class, but we need to know enough to navigate the filesystem and execute the `python3` command. If you need assistance getting started with this step, your best bet is to contact the instructors. Each student's computer is a bit different, so it is difficult to cover all possible cases here.

{{% /notice %}}