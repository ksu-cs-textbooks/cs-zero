---
title: "Tic Tac Toe JS"
pre: "13.7 "
weight: 35
date: 2020-08-28T16:27:26-05:00
---

{{% notice tip tip-1 "JQuery Script Tag" %}}

In some older videos, the JQuery script tag is shown using `http` in the URL. This should be changed to `https` in order to work correctly due to some recent browser security updates. Alternatively, you can always find the correct JQuery script tag by visiting https://releases.jquery.com/ and clicking the "uncompressed" link next to the latest version of JQuery. 

{{% /notice %}}

{{< youtube eompYk6zR6Q >}}

<!-- TODO Rerecord Video -->

#### Resources
* [Slides](../slides/14-WebProgramming2.pdf)

#### Video Script

Welcome back everyone. In this video, we're going to start making our Tic Tac Toe game a little bit more interesting by enabling us to actually play the game. So a few pieces that we need before we actually start programming with the JavaScript. The first part is our script tag. So we need to actually embed JavaScript into our web page. So to do that, we're going to add a couple tags, right after our table or our board that we had before. So down here towards the bottom right above your body tag, right underneath the table tag, we're going to add our script tags. And these script tags are going to be used to import the JavaScript. So just like what we've done with our CSS up here, where our link tag is actually importing our CSS, our Cascading Style Sheets into our page. Our script tag is going to work very much the same. So I'm going to go ahead and just paste these in here. And then let's go ahead and talk about them. So each script tag has a source attribute, where the source attribute is going to be the actual location of the script that you're actually pulling in. And inside, typically, you won't see one unless you're importing JavaScript. Typically won't see anything in between the opening and closing tag, but you could just leave the source blank, and actually put the JavaScript straight inside of the tag itself. 

But in this situation, we're importing two different things. The first one is jQuery. Now, we've talked about jQuery before. jQuery is the JavaScript library that enables us to manipulate and modify the DOM elements on the web page in a way that is a little bit easier to utilize than raw JavaScript itself. And then the second script tag, there is going to be our Tic Tac Toe JavaScript that we use to play our game. So let's go ahead and save that out. Now, nothing is going to change as part of our web page here. So our JavaScript still stays the same as we had before. But let's go ahead and create our JavaScript. So in our, and you may need to create a new file here if you don't have one already. So let's go ahead and change this to all types. I'm going to call this script.js for JavaScript. And on our next slide here, we actually have all of the JavaScript that you want to actually put onto your web page. So let's go ahead and copy this over. Now, do be careful when you're copying and pasting this particular chunk of code because whitespace can make a difference here, depending on what you're copying and pasting from. So just be careful with the whitespace and spaces. So everything should match up exactly as I have it. So just to explain our JavaScript here just a little bit before we move forward here. 

JavaScript is very similar to how Python works in the sense that it is a dynamically typed language, meaning that we don't actually have to declare data types. But variables in JavaScript are typically declared using something, a keyword called let or var. So we have a variable called turn, it is initially x, because x always goes first. And then here, every everywhere you see a $ is referring to the jQuery library that we actually imported. So what the dollar sign is going to do is it's going to select. This is going to select all of the DOM elements that match this search or this search parameter. And so this search here is going to be looking for td tags. And the search is very much based off of the CSS rules that we've had before. So the selector or the search, or this query is going to look for all the td tags, and then it's going to link to it this onClick event. So this function is going to be ran or executed, every time a td tag is clicked. When the td tag is clicked, we're actually going to select that square. 

So we're going to take that square or that td tag that was selected. And then if there is no data inside of it or text inside of it, so meaning that there is no X or there is no O, we're going to insert the text for whoever's turn it is. So if it's X's turn, we'll add an X. If it's O's, turn we'll add an O, and then we'll change turns. And lastly here, at the end of our click, we need to update the div tag that we had before with new text that indicates whose turn it is an actual game. So if we save that out, and then go back over to our webpage and refresh, and we click, we can see that our page actually updates with X's and O's. Now, you can see here that it actually alternates, but it's not going to recognize when you win, or lose. So that will just kind of a scouts honor sort of thing. We're not going to code this up to indicate whether or not there's a winner or loser in this class. But it's still kind of a fun little exercise all with CSS and JavaScript that we can make a really simple game in a relatively short amount of time. 

