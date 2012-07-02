---
layout: post
title : The World is Parallel
summary : Supporting programming in a craft-first electronics course.
category : software
author : Matt Jadud

tags : 
 - earlydays
 - parallel
 - visual
 - occam
 - transterpreter
---

A first course in electricity does not necessarily need to touch on programming. In fact, a first course in electronics does not, either... especially if you 1) stay strictly in the analog realm, or 2) branch into the digital realm, but completely avoid the microcontroller. As a computer scientist (and, more importantly, someone who likes to make cool stuff that interacts with the world), it is hard to imagine leaving out the microcontroller when digital electronics.

An introduction to electricity and electronics that grounds students in the safe design and fabrication of electronics for themselves (not for industrial-scale mass-manufacturing) is going to need a microcontroller. And while the Arduino is wonderful, the fact is that I simply do not want to teach someone C++ so that they can get a simple digital electronics system up and running. Likewise, most visual tools (Ardublocks and the like) don't handle doing two things "at the same time" well at all.

While we've been designing curriculum, I managed to hack together a prototype visual environment for programming the Arduino at a high level. I'm calling it **Ardu See, Ardu Do** in the spirit of [If This, Then That](http://ifttt.com/).

<div align="center">
<a href="/blog/images/ardu-see-ardu-do-prototype.png"><img src="/blog/images/ardu-see-ardu-do-prototype-thumb.png"></a>
<br/>
<em>The Ardu-See-Ardu-Do prototype. (Click for full-size image.)</em>
</div>

<br/>

The back-end of this system doesn't really bear describing... it's a cobbled together collection of tools, including one or two copy-and-paste steps. However, every step we engage in can be scripted or collected up into a single application. And, the important thing is that a program like the one above is (programmatically) turned into code that looks like:

<br/>

<pre>
PROC main ()
  CHAN INT wire01:
  PAR
    TurnSomethingOn(4, wire01?)
    SensorinRange(A0, 50, 100, wire01!)
:
</pre>

<br/>

It is possible you're not familiar with the [occam-pi programming language](http://occam-pi.org), or the fact that there is a virtual machine for the Arduino called the [Transterpreter](http://transterpreter.org/). occam-pi is important because it is a small language that makes it easy to do multiple things concurrently (on the Arduino) or in parallel (where you have multiple processors). In the case of "Ardu See, Ardu Do," we want it to be easy for a novice to (for example) link multiple LEDs at the same time.

<br/>

<div align="center">
<iframe align="center" width="560" height="315" src="http://www.youtube.com/embed/UGxn-zpw-U8" frameborder="0" allowfullscreen></iframe>
</div>

<br/>

Although the dinosaur-laden video included above was not written with "Ardu See, Ardu Do," it could have been, easily. I make this claim mostly because I wrote the code that is running in the video, and know that I could make this (prototype) tool emit the code to do the same thing as shown above. We'll have to try and do that... perhaps tomorrow, even.

But for now, it's midnight, and it really is time to call it a day. Two hours of hacking took the prototype from "it looks good, but doesn't do anything" to "it generates code." We'll do some experimenting with the Arduino tomorrow (which, for a variety of reasons, we know will work), and from there we'll have to start making some decisions about how much more time should be invested in taking this from **hack** status to **use with students in a classroom**.

We'll also get the code into a repository, so that interested parties can contribute (if they are so inclined).