---
layout: post
title : Ardu See, Ardu Do
summary : Visual, parallel programming for the Arduino.
category : software
author : Matt Jadud

tags : 
 - earlydays
 - parallel
 - visual
 - occam
 - transterpreter
 - nodejs
 - javascript
 - scheme
---

## Academese 
I've enjoyed working on the <a href="http://transterpreter.org/">Transterpreter project</a> for some years now. This is a virtual machine that makes it possible to run <a href="http://occam-pi.org/">occam</a> programs on a variety of embedded platforms.

## Plain English

<div class="well">
  <div align="center">
    I make <a href="http://concurrency.cc/">tools for the Arduino</a> that let people easily do two things at (almost) the same time.
  </div>
</div>

That said, there's a catch. To do this, you have to learn how to program in occam, an old programming language that was designed for a long-dead processor. However, the language did make it easy to write safe, parallel software for embedded devices like the Arduino. The problem has, for some time, been this: **how do you make it easy for beginners to do hard things as easily as possible on the Arduino?**

## Ardu See, Ardu Do

Over the past week or two, I've hacked together a prototype system that lets a user drag-and-drop blocks of functionality around, wire them up, and send the resulting program to the Arduino. This short video explains in pictures better than I can in words:

<!-- http://youtu.be/hdZys5dUxEQ -->

<div align="center">
<iframe width="640" height="360" src="http://www.youtube.com/embed/hdZys5dUxEQ" frameborder="0" allowfullscreen></iframe>
</div>

I will admit, I'm not keen on the name, so suggestions are welcome. But, I am **very, very excited** about the possibilities here. While tools like <a href="http://blog.ardublock.com/">Ardublocks</a> and <a href="http://www.modk.it/">Modkit</a> are cool, they still require you to think *sequentially* about systems that are fundamentally *realtime and parallel*. A dataflow environment lets you think about where data enters your system, how you want to modify it, and what you want to do with it when you're done---be that turning on an indicator LED, running a motor, or posting data to a web service. In short, a dataflow language makes it easy to have a Sense-Think-Act cycle, and a parallel-safe language makes it easy to have many small cycles working together.

In short, this could be developed into a robust rendition of <a href="http://ifttt.com">If This, Then That</a> for the Arduino.

# Dream Big

We have an <a href="http://concurrency.cc/">incredibly robust foundation for parallel programming</a>, and are working on designing a <a href="http://craftofelectronics.org/">craft-first introduction to electronics</a> that does not bury students in equations, but instead has them designing, building, and testing systems as a way of exemplifying the underlying theory of electrical and electronic systems. These things put together have lots of potential... but, probably not in a 14-week semester.

However, a simple, visual environment for describing parallel-safe dataflows is a transformative way to think about prototyping electronic systems, be they <a href="http://hackaday.com/2010/05/14/cat-door-unlocks-via-facial-recognition/">homebuilt home automation  equipment</a>, or <a href="http://www.youtube.com/watch?v=_RyodnisVvU">small robots built for personal enjoyment</a>.

# Contributing

If you're interested in this project, ping <a href="http://twitter.com/#!/concurrencycc/">concurrencycc</a> on Twitter, join a concurrency.cc <a href="http://concurrency.cc/docs/mailinglists.html">mailing list</a> (developers or users, as you see fit), or (if you're interested in the craft of electronics project), join the <a href="">CRAFToE Google Group</a> and introduce yourself.

1. The backend (running on the Arduino) requires no work---packaging, maybe. Scripting the execution of the compiler, yes. But no hard or otherwise fundamental effort is required.
1. The frontend (GUI) may need a complete redesign. But, there's a lot of good material to work with, and someone whizzy with JavaScript and CSS could easily do a lot to improve what is there.
1. The GUI and server process could be replaced with a native application... if there was a good graph component library to build on top of. 

The code is on Github. It is an undocumented hack that runs on my machine. It requires Node.JS, the Transterpreter (occam-pi) toolchain, a recent version of the Racket (nee Scheme) programming language, and probably a few other things I haven't thought of. However, if there is interest, I'm happy to rewrite/scrap/support any reasonable explorations that help move this idea forward.

# Crunchy Details

An introduction to occam via the Plumbing library is available in <a href="http://concurrency.cc/book/">a short book we've written</a>, and more resources can be found online on some <a href="http://rockalypse.org/courses/cs220f11/guides/introducing-occam-pi/">course webpages of mine from last fall</a>.

For the interested, here is the occam program that is generated from the diagram demonstrated in the video:

<pre>
#INCLUDE "ardu-see-ardu-do.module"
PROC main1341371708 ()
  CHAN INT wire01, wire23:
  PAR
    ReadSensor(A0, wire01!)
    TurnOnInRange(8, 50, 100, wire01?)
    ReadSensor(A0, wire23!)
    TurnOnInRange(9, 0, 49, wire23?)
:
</pre>

And, the implementation of the two blocks that you see running in the demo:

<pre>
#INCLUDE "plumbing.module"

VAL INT READ.DELAY IS 100:

PROC ReadSensor (VAL INT pin, CHAN INT out!)
  INITIAL INT avr.pin IS board.analog.to.chip(pin):
  WHILE TRUE
    INT reading:
    SEQ
      delay(READ.DELAY)
      adc.base(avr.pin, VCC, reading)
      out ! (reading / 11)
:

PROC TurnOnInRange (VAL INT pin, min, max, CHAN INT in?)
  WHILE TRUE
    INT value:
    SEQ
      in ? value
      IF
        (value >= min) AND (value <= max)
          digital.write(pin, HIGH)
        TRUE
          digital.write(pin, LOW)
:
</pre>

