---
layout: post
title : We build things too!
summary : It's Friday afternoon. Let's take a break from theorizing about curricular design and have fun Making Stuff from Things We Have In Boxes.
category : coursedesign
author : Mel Chua

tags : 
 - earlydays
 - handson
---

We've been spending all of this week high up in theory-land. While that's great, it's nice to counterbalance it once in a while -- so we decided to get our hands dirty today and make something cool (and then analyze it from a curricular perspective once it was done, I'm sure).

So we looked at the little robot Danny was building and the contents of the small box of random components Matt had taken with him from Pennsylvania. This was the equivalent of a couple chefs opening the fridge to make dinner and finding a potato, a container of Kit-Kats, a jar of peanut butter, and a tub of shrimp paste; strange constraints breed strange improvisations.

We ended up deciding we wanted music in the lab (which doesn't yet exist; we're working in the hallway of the Tech building while it's under construction) and that it might be fun to control it in interesting ways. Imagine a box with a button on it sitting atop a speaker. Music streams through the room, issuing from aforementioned speaker. When you push the button, the music pauses; push again, and it resumes. But as you walk away from the box, you notice that the music's getting louder -- the box is also sensing your proximity to the speaker and adjusting the volume accordingly. Ooooo!

Okay, we had an ultrasonic rangefinder and some giant arcade-style momentary-on pushbuttons, and wanted to make something that would be flexible/extensible/cool. Grooveshark seemed like a fun API to play with. Why not?

For extra fun, we're also outputting the raw value of the distance sensor as the position on a servo, and the volume level it's adjusting the music to via a bank of LEDs.

After a few hours, we have most of a working prototype circuit, a laser-cut cardboard faceplate for the whole shebang, [half-finished Wiring code](https://github.com/barnesdannya/Grooveshark-Controller-Box "Grooveshark-Controller-Box on Github") for the Arduino that binds the thing together, and a knowledge of what we need to do in Python to finish on Monday.
