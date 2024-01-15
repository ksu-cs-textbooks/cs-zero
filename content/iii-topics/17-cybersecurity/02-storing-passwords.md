---
title: "Storing Passwords"
pre: "17.2 "
weight: 10
date: 2020-10-24T00:27:26-05:00
---

{{< youtube ct5h7u-PD4o >}}


#### Resources
* [Slides](../slides/23-Cybersecurity.pdf)

#### Video Script

So finally, let's talk about storing passwords securely in your applications. And there are a lot of different ways you can store passwords so that users could use them to authenticate. Let's take a look at that. First, obviously, we could store the password itself. The user types in a password, we store that password in the database. Great, right? They type that password in again, we check it to make sure they typed in the same password. If they did, they let them in. That sounds like a really great system, doesn't it? Hopefully, you're cringing a little bit thinking about this. Because obviously, websites that have databases on them get hacked all the time. And if a hacker gets access to this database, they have your password. Simple as that. There's nothing that they have to do, there's no decryption they have to worry about, they get your password. And of course, one of the weaknesses of people on the internet is we tend to use the same password over and over again. Raise your hand, if you do that. I do. I use the same password a lot of places on the internet, it's something I probably shouldn't do. But I do. And so if somebody gets one of my passwords, they might be able to use that password to log into other websites that I use that same password on. So this is obviously not very secure. And the only thing that they need to compromise this is database access. As soon as they access the database, they have all the passwords, and it's really simple so we probably shouldn't do this. 

What if we store the passwords by encrypting them using a key? Well, that makes them a little bit more secure, which means now if you get the database, you also need to have a key to decrypt the passwords, or of course, some sort of a lookup table or a rainbow table to decrypt the passwords. And so you know, as soon as they get the database in the key, it would compromise all the accounts. So this is better than storing the raw passwords. But it's still not great. And it's not that hard. T

he really best way to store passwords is using what's called a password salt. And this is because users are generally bad at creating good passwords. And so what we can do is take their short, crappy passwords and add a long string of random characters to it before we encrypt it. And so that will make the encrypted password much much stronger, it will feel like a longer password, even if the user's portion of that password is very short. So it protects against all sorts of things like dictionary rainbow table attacks, Rainbow table attacks assume that passwords are pretty short. Most rainbow tables only work on passwords that are 10 characters or less. So if we add a salt of 25 characters to the end of a password, we're guaranteed to get something that's pretty long and hard to break using just standard encryption attacks. So if we store with a global salt, which means that we use the global salt value, the same salt value for all passwords, then a hacker would have to get the database, the encryption key we used, and that global salt value. And the nice thing is those are typically stored in three different places. The database is stored, obviously, as the database. The encryption key is probably stored somewhere in the software, and the salt value is probably stored somewhere in the software's configuration. And so you need to get all three of those parts to break these passwords. If you didn't have the encryption key or the salt value, you could try and brute force it, but it would take a long time. The downside is once you brute force a password, you could get the key and the salt and use that to compromise all the other accounts. So if you get one, you still get all the accounts compromised, but it is a little bit harder to do. The other thing you can do, of course, is you can encrypt all the passwords with a unique salt value. So every single user, every single account gets its own salt value. And if you do that, you need the database encryption key and the salt value for each user account in order to crack it. And that makes it even much harder. That means you can only compromise one account at a time, because every single time you need to get that salt value for that account. And so that makes cracking these passwords really, really hard to do. 

So lastly, let's take a look at one of the instances where people have really broken passwords very, very quickly. And this is from the Adobe hack from several years ago. And again, this is an XKCD comic. But what happened is Adobe misused an algorithm called block mode ds. And what that does is every block of your password gets chunked up. So every eight characters or so it gets broken, and it gets encrypted separately. And because they did that incorrectly, if the user had the same password in that first eight characters, it would encrypt to the same thing. And so what you end up with is basically the world's largest crossword puzzle. So for example here you would have weathervanessword and then you have name one. If you're a fan of redwall, you might understand that weathervanessword might have something to do with Matthias from redwall and so this might be Mateus1. Here you have favorite of the 12 people apostles - Matthais, and then you have all these other ones like alphaobviousmichaeljackson. I'm guessing this is ABC123- the famous Michael Jackson hit from when he was in the Jackson5. It's an obvious password, and it's alphabetical. So there are lots of different examples of bad passwords, being stored improperly not correctly salting and hashing them like you should and this is one that Adobe definitely got called out for back in the day. So finally, if you want to take a look at your own passwords and see how secure they are, there's this website howsecureismypassword.net. You can go online you can type in your passwords and it will give you an idea of how long it would take to crack that password.