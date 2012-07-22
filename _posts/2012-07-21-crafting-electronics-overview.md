---
layout: post
title : Crafting Electronics
summary : A first course in overview.
category : software
author : Matt Jadud

tags : 
 - safety
 - design
 - fabrication
 - thinking with hands
---

We've been working hard all summer to frame a new, first course in electronics. We are thinking in terms of *craft*: making just one thing well, by hand. This has led us to realize that safety, design, and basic electronics fabrication skills are essential to the novice student of electricity and electronics.

# The Course, in Brief

## Week One: The Framing Experience

During the first two days of class (a half-week), we will start with a short exploration of soft circuits. The purpose of this is twofold: first, we immediately engage students in a successful electronics experience, and second, they see on day one that electronics is not necessarily equations and circuit boards. We are considering the [LilyTiny](http://www.sparkfun.com/products/10899) as a backbone for this first experience, and think [Lovell, Ji, and Freed's plush monsters tutorial](http://web.media.mit.edu/~emme/monsters.pdf) (PDF) is representative of what we want them to do on their first two days.

## The First Half: The Quantified Self

At the start of the semester, we will engage in a series of skills activities to master the basics of soldering, culminating in the build of an Arduino kit (perhaps either the [RBBB](http://shop.moderndevice.com/products/rbbb-kit), [JeeLabs JeeNode](http://jeelabs.com/products/jeenode)) and battery-based power supply ([MintyBoost](http://www.ladyada.net/make/mintyboost/) or similar). This will allow us to explore, week-by-week, a series of sensors that allow us to reflect meaningfully on our own behaviors and the impact those behaviors have on our own health, the health of those around us, and the world.

We have experience with this kind of build from previous courses; for example, we've worked with students of Environmental Science and built room usage sensors that monitored light levels. These sensors allowed students to tell when the lights were on (but nobody was home), and in doing so, help shape institutional policy and direction regarding the purchasing of sensors to automate the turning off of lights around campus. We reported on this (along with some of our lower-level work on parallel-safe runtimes for the Arduino) at Communicating Sequential Processes 2011 in a paper titled [Concurrent Event-driven Programming in occam-pi for the Arduino](http://christian.lyderjacobsen.com/publications/index#Jacobsen11).

## The Second Half: Home and Environment

At the midpoint of the semester, we will shift our focus from digital electronics and our own behaviors to the home and environment around us. Students will start with practical electrical skills on a small scale: wiring switches, lights, and the like. (Although it may seem pedestrian, safety and practice with home-level voltages is, we think, essential.)

Although we will then step out further (and study the theory and practice of home wiring on a whole-house scale), we will do so by working on a smaller scale, with model houses. Students will use these for two purposes: first, to explore the complexities of wiring a "real" house, and second, to develop a home sensing/automation project and "deploy" it into their own (model) home. 

# Highlights: Simplicity and Context

We are particularly proud of two aspects of the course. First, we have developed a new programming environment for the Arduino that will, we believe, make the programming of complex behaviors possible with a drag-and-drop dataflow interface. Second, we have grounded our study of home wiring and automation in fully in the context of the Appalachian region, which is critical in the context of Berea College.

## Flow: A Simple, Visual Arduino Environment

Over the past six weeks, I brought together a collection of high- and low-level tools to create a new, visual environment for the Arduino. It is different from all other environments available in that it allows the user to specify the **flow of data** as opposed to the **flow of control**.

This short video demonstrates better than I can describe:

<div align="center">
<iframe width="640" height="360" src="http://www.youtube.com/embed/hdZys5dUxEQ" frameborder="0" allowfullscreen></iframe>
</div>

We are confident this environment will allow students to quickly and easily explore new ideas in digital electronics without us having to teach them how to write code. Although environments like ArduBlocks and Modkit are compelling, they still require students to master sequential, C-style programming. We want something lighter, faster, yet more powerful.

There is a great deal more we could say. For now, [you can download a (very, very alpha!) prototype of this environment for Windows, Mac, or Linux](https://github.com/craftofelectronics/flow/downloads), and explore it on your own. Please [join the users@concurrency.cc mailing list](http://concurrency.cc/docs/mailinglists.html) if you have questions, and [developers@concurrency.cc mailing list](http://concurrency.cc/docs/mailinglists.html) if you would like to help improve anything about the software, be it the interface (HTML/CSS) or back-end (Scheme, C, and occam-pi). (Flow's source [lives on GitHub](https://github.com/craftofelectronics/flow).)

## The Berea Contrast House

The context for the second half of the course is the Berea Contrast House ([wiki](http://bereapedia.wikispaces.com/Contrast+House), [images](http://cdm272901.cdmhost.com/cdm/search/searchterm/Contrast%20House,%201935-/mode/exact)).

<p align="center">
<img src="/blog/images/berea-contrast-house.jpg">
</p>

It is our intent to work with Paul and Julie Campbell of [MakeCNC.com](http://makecnc.com/) on the design of a CNC-ready (laser or router) model of the Berea Contrast House. This house played a fascinating role in the history of the college, and there is still one standing nearby. As part of the course, students will cut (using the laser cutter) their own house, build it, and then use that model for demonstrating how they would lay out the wiring in a small house. They will then use their Arduino to add home automation features, and present their final designs as part of an exhibition at the [Berea College Appalachian Center](http://www.berea.edu/appalachiancenter/).

It is our hope that the model house design will be freely licensed under a Creative Commons license, allowing others to make and explore the same ideas using the Contrast House as a starting point for their explorations.

# Conclusion 

Given that the students of Berea College are predominantly from the Appalachian region, our course design lets us ground the safe design and fabrication of electronics fully in their personal experience and cultural/historical context. 

<p align="center">
<img src="/blog/images/safety-design-building.png" alt="Enduring Understandings for the Craft of Electronics"/>
</p>

Each of these *enduring understandings* are connected by three *enduring transitions*:

<p align="center">
<img src="/blog/images/thinkinghands-itertrans-theorytest.png" alt="Enduring Transitions for the Craft of Electronics"/>
</p>

We have been working hard developing infrastructure as well as planning the course down to 15-minute intervals; we have post-its *everywhere*. We're working hard to share as much of our process as possible, and will share as much of the course materials (laboratories, assignments, etc.) under a CC BY-SA license wherever and whenever possible. 

# Join Us

If you are excited by the work we're doing, please [join our mailing list](https://groups.google.com/forum/?fromgroups#!forum/craftofelectronics) or [follow us on Twitter](http://twitter.com/craftoe). Let us know what you think and how you might like to get involved.