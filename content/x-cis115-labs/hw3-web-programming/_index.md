+++
title = "Web Programming"
date = 2022-02-18T00:23:05-05:00
hidden = true
pre = "<b>HW 3. </b>"
+++

## Web Programming

In this assignment, we're going to explore how to build a website on the CS Linux servers using HTML, CSS, and JavaScript. This will give you all the tools and information you need to start building your own personal website that can be hosted for free on K-State's systems.

{{% notice note note-1 "Learning Objectives" %}}

The goal of this assignment is to demonstrate understanding of the following topics in Python:

* Linux Terminal and SSH Basics
* HTML
* CSS
* JavaScript

{{% /notice %}}

## The Assignment

Your assignment is to build a personal webpage on the CS Linux server or a personal web server/host if you so choose. Your site must be publicly accessible. Your grade will be based off of the URL submitted to Canvas **AND** the source files submitted to Canvas.  This is an individual assignment.   

Your site must contain 3 different files: `index.html`, `about.html` and `fancy.css`. They are described in detail below.

### HTML Page Requirements

Each HTML page on your site must, at a minimum, include the following items (more is perfectly fine): 

* Valid HTML5 code - use the [W3 Validator](http://validator.w3.org) to check that your HTML is correct
    * You may ignore any errors about character encoding
*  A `<head>` section that includes:  
    * The site's title in a `<title>` tag 
    * A reference to the site's CSS file in a `<link>` tag, such as `<link rel="stylesheet" type="text/css" href="fancy.css">`
* A `<body>` section, containing your HTML content, which includes:
    * A header defined by the `<h1>` tag at the top of the page 
 
### Index File

Your `index.html` file is the homepage for your website. It should include the following, in addition to the HTML page requirements listed above:

* 4 paragraphs of text using the `<p>` tag. 
    * The paragraphs should be long enough to line-wrap a couple of times. Feel free to include placeholder text from Lorem Ipsum, one of your discussions, or elsewhere. 
* At least 1 word in each paragraph should be bolded using `<strong>`.
    * It is better to use `<strong>` than `<b>` since the former implies the intent, not just the style.
* At least 1 word in each paragraph should be italics using `<em>`. 
    * It is better to use `<em>` than `<i>` since the former implies the intent, not just the style.
* A working link to your `about.html` page in an `<a>` tag (it should be a relative URL, not an absolute path) 
* A working JavaScript Tic-Tac-Toe game (as shown in the videos and in class) 
 
### About File

Your `about.html` file gives a bit more information about yourself. It should include the following, in addition to the HTML page requirements listed above:

* 1 ordered `<ol>` or unordered `<ul>` list containing at least 4 list items using the `<li>` tag. 
    * Feel free to include your favorite movies or TV shows in the list. 
* 1 working link to your favorite site using the `<a>` anchor tag (this should be an absolute path). 
* 1 embedded image using the `<img>` tag. 
    * Choose a favorite image from Wikipedia to include on your site if you don’t have one to share. 
* 1 embedded resource (Youtube Video, Twitter Feed, etc.) 
 
### CSS File

Your `fancy.css` file contains directives that are used to style your website. It should include directives to do the following: 

* Change the font used in your paragraph tags 
* Change the size of text in your headers 
* Change the color of text in your anchor (link) tags 
* Change the background color of your page (_no neon colors, please_) 
 
## Submitting
 
Submit the public URL of your `index.html` page (as an assignment comment) **AND** upload a ZIP file containing all of the HTML and CSS files used in your website to the assignment on Canvas.
 
## Resources

Below are some helpful resources for completing this assignment:

* Videos and Slides on Canvas 
* http://www.putty.org/ - Download PuTTY for Windows Users 
* https://filezilla-project.org/ - Download FileZilla for Windows and Mac Users 
* https://support.cs.ksu.edu/CISDocs/wiki/Personal_Web_Pages - CS Support for Web Pages 
* http://www.w3schools.com/html - HTML Reference 
* http://www.w3schools.com/css - CSS Reference 
* http://www.w3schools.com/js/ - JavaScript Reference 
* http://validator.w3.org - HTML5 Validator 
* http://www.w3schools.com/html/html5_canvas.asp - HTML Canvas Example
