---
title: "The Interactive Web"
pre: "13.4 "
weight: 20
date: 2020-08-28T16:27:26-05:00
---

{{< youtube ZAO8aBXMKyY >}}

#### Resources
* [Slides](slides/14-WebProgramming2.pdf)

#### Video Script

Welcome back everyone. In this video, we're gonna be taking a look at interactive web technologies. And now we've talked a lot about these things in the past about Web 1.0 vs 2.0. So going from the static plain HTML Web to Web 2.0, where everything is much more dynamic, interactive, more media, more content, more interactive technology. And so we're going to take a look at how we can actually use some of these to make our websites a little bit more interesting. Some of the primary ones that we'll be talking about today are the Document Object Model, which is fundamentally how a lot of the Web 2.0 pages actually are structured and work. JavaScript, Ajax, and JSON, which also helped make our webpages a lot more interactive. First, let's take a look at the Document Object Model or DOM. So the document object model is really how a web page is actually structured. So you can kind of think of the window here as like a tab in your web browser. So the entire contents of that is your window. And in that window, we have history of that web page. So maybe even things like cookies, past searches, past form information, things like that, location information. But then we have the document itself, which is the actual page that we've loaded. So your document or HTML, everything that was between the open and close HTML tags, actually goes here. 

But this operates kind of like a tree structure here. So the base form here, the base is going to be our HTML tags. And then we can kind of dive deeper down in that way. Like, for example, we have the anchor tags, which are links in our web page. Or we could even have a form like if we're trying to sign up for a website or making a post on Reddit or something like that. So we have basically everything that we can interact with, or click on or work with on our webpage is contained inside of this document. But this gives us a lot of structure as well. So when we're actually trying to make dynamic and interactive content, having the Document Object Model allows us to manipulate and work our web page, whether or not that is inserting new elements into our web page, or modifying those elements on our web page. So the the root element here is the document itself. So that's the top of our tree there. And from our document, we go down into the root, actual HTML tag, and then everything else is kind of contained in between. 

So before we had the header tag, and if you remember, the header tag doesn't actually contain information that's typically displayed on web page itself, but has information that is important to the webpage to render, for example, the title which is shown on your tab inside either Firefox or Chrome. So the head tag contains in this case on this page has a title tag and that title tag has some text. And so that is the actual content of that particular tag. Each tag here is considered an element of the DOM. So each tag is going to be considered an element, each tag contain any number of more tags. And those tags can also contain other types of content, like text. Now, the primary source of content on our webpage was the body tag, if we remember, right. T

he body tag is going to contain everything else that we had on our page, like we have a head tag here, for example. The head tag has some text. This a tag those one becomes a little bit more complex. So we have the a tag, which is our element. The a tag can also contain the attribute href, which contains the information on where that link is actually going to. So if it's a different web page, if it's a different image, whatever we're trying to actually navigate to. And then we have the link text as well as part of the a tag. So you can kind of start to imagine how this rigid structure of the actual HTML allows us to navigate this a little bit better. Because without this, an HTML web page is actually just really kind of a jumbled mess. 

So thanks to the Document Object Model, we have a relative standard that we can use to actually search our web page dynamically in order to insert, add, or change anything as part of our webpage, after the web page has loaded or while the web page is being loaded. So this allows us to have again, right we're going from a very static webpage that never changes, unless we actually change the webpage by hand on the backend if we upload a different file to our server to Web 2.0 where we're having a little bit more interaction here and more dynamic content. So now instead of having a plain single web page, my webpage can actually change as it's being loaded or changed based off of who's logged in. This adds a lot more purposeful information to our websites. But in this series of videos, what we're going to start taking a look at is how we can make a tic tac toe game in HTML. 


