---
layout: post
title : Enduring understandings
summary : What do we want students to remember 5 years after they take the course?
category : coursedesign
author : Mel Chua

tags : 
 - earlydays
 - personas
---

# The Very Big Picture

Matt arrived at Berea on Monday; Sebastian and I got in Thursday night, and the entire CraftOE team finally met face-to-face on Friday. After finding me and Sebastian places to sleep (couch cushions on Matt's living room floor) and food to eat (salami sliced on the overturned lid of a blue plastic moving bin), we declared Berea Coffee & Tea "mission headquarters" (at least until internet connectivity arrives at Matt's house) and set to work on curriculum design. Today's accomplishment: a first pass on **enduring understandings.**

## Enduring Understandings, first draft

 We have 6 hours a week for 15 weeks in-class with students; that's not much time. *If students only remember 2-3 things 5 years after they finish 90 hours of our class, what are the things we'd want them to remember?*

1. **How to play with electricity and not die.** To safely and practically deal with live wires, large capacitors, static electricity, unknown circuitry, and so forth (while rewiring a 3-way switch, or replacing an electric outlet, or repairing a monitor, or...)
2. **To believe their experience and build it incrementally.** Students should be empowered to tackle problems -- especially complex problems with no immediate clear solution in sight  -- by incrementally building, testing, and debugging all aspects of it one step at a time. They should be confident in trusting their empirical evidence over documentation when the situation warrants it; components can be off-tolerance, specifications might not be fully implemented, documentation might be inaccurate. Use documentation, but trust and test your observations over your reading.
3. **Translate between written, visual, and physical representations of circuitry.** Students should be able to translate between a breadboard, a circuit board, and a circuit diagram. (A sample assessment for this: given the breadboard, circuit board, and circuit diagram for 10 different circuits, match them into triplets.)

## Personas, first draft

How did we check whether our targets for enduring understanding might be reasonable? Personas. We sketched out (loose, rough first drafts of) four imaginary students in the class and looked at what might be most useful for them to remember.

1. **Annette** is a 2nd-year Biology major taking Electronics to fulfill a distribution requirement. She would benefit from (and likely resonate with) #2, "believe your experience and build it incrementally," since modern biology involves fine detail work that takes keen observation and rewards a careful step-by-step exploratory approach.
2. **Bob** is a 1st-year Technology major who's more interested in Metalwork than Elecrtronics. He says he's "not so good at math," and plays guitar on campus. Bob needs to be able to safely deal with electricity (#1) and understand schematics (#3) for the CNC machines he'll work with in the future -- because tools don't always function as perfectly as planned.
3. **Cathy** is a 1st-year student who was the "equipment gal" for her high school chapter of Future Farmers of America. She likes home DIY and hanging out with her dad's ham radio buddies, and would rather spend time building things than learning theory. She'll need safety (#1) for her hands-on explorations as she builds on her experiences (#2) and uses the documentation (#3) for the equipment she's working on to make her explorations swift and deliberate.
4. **Dwayne** is a 2nd-year student thinking about a 3-2 program in Computer Engineering. He's never met a CE, but he's heard engineering has good career and income prospects, and he enjoyed building his own computer in high school, so why not? Dwayne will need to build his systematic debugging skills (#2) to prepare for advanced engineering college classes and needs to be prepared to understand the theoretical readings (#3) he'l encounter there.

## Other loose goals, learning objectives, and ideas we tossed around today

* **Technology is a social construct** -- "this stuff" (connector designs, communication protocols, programming languages, specifications etc.) isn't handed down on stone tablets from On High; it was made by groups of people deciding things like "the USB connector ought to have 4 wires" ("Yeah, I guess 4 would be fine." "Okay, it's 4 wires then!"), and you could help design these specifications yourself. Groups of people aren't always right, and the things they make evolve over time. (This isn't written in the format of a learning objective, but we thought Annette, Bob, and Dwayne would benefit from this understanding nevertheless.)
* **Solder and desolder with confidence.** Bob, Cathy, and Dwayne in particular would use this skill in the future.
* **Match up a component with its functionality.** Cathy and Dwayne would likely appreciate this most. I struggle to describe this as a learning objective, but if I may jump ahead to describe an activity that address it: students are handed a simple unidentified component; op-amps, oscillators, transistors, voltage regulators, and things of that class. (Multiple students might have the same type of component, but of different varieties and from different manufacturers.) They're expected to use the markings on the DIP package to find the component's datasheet, then use the datasheet to build a basic demo circuit for that component and present its functionality to the rest of the class in science-fair-poster-exhibition style. (Education folks: what's the learning objective(s) underlying this activity?)
* **Understand that microcontrollers aren't magic** - all they're doing is turning things on and off, and there's a datasheet that tells you exactly what they do.
* **"What is the right level of abstraction to use under what circumstances?"** This was shelved as a goal that was too subtle and meta to build into a first electronics course, but the general idea was that students should know when to "pop the hood," roll their own solutions, or use low-level components, and when to use COTS (components-off-the-shelf), high-level prototyping languages, existing libraries, or sketch models. It's something you learn from experience.

# Next steps

## What's craft?

It's in the early days. We're still trying to figure out what "craft" means -- as computer scientists and engineers, our training has been in a very different learning modality, so we're visiting at least one craft shop every day to try and get a better sense of craftsmanship culture (yesterday: dulcimers! today: glassblowing!) and looking forward to meeting and learning from the expertise of the artists and craftspeople around us. We *have* discovered that Berea Tea & Coffee makes excellent iced cappucinos, so we'll be back for more tomorrow.

## What's next?

We'll continue to move towards learning objectives in the morning -- first we're figuring out what students should learn (content), then we'll think about how to tell whether they've learned it (assessment), and *then* we'll think about activities to help them get there (pedagogy). 

## Questions for our friends out there on the intarwebz

1. Are we missing any student personas? (You may want to read about [Berea College][http://www.berea.edu] first for context.)
2. What do you think the enduring understandings and learning objectives for a craft-first intro electronics course (the first of a 2-course series) ought to be, and why? Which personas (from the list above) would benefit from them, and how?
3. What do "craft" and "craft-first" mean to you, in the context of "the craft of electronics"?
