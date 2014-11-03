# Design notebook for week ending November 2, 2014

## Description

This week, I decided which of my ideas would be worth extending into a language. I decided to extend the tone-matrix idea, which is beautiful in its simplicity, and corrupt this simplicity slightly to allow for greater functionality. 

A number of open questions remain as I begin to move into this project:

* Which language should I use to implement this language?
* How will I design and implement the link from tones to colors? 
  * What APIs allow the control I want? 
  * Which qualities of sound make the most sense to present to the user?
  * How do I want the user to control this? (see Questions section)

I'm currently looking into what, exactly, the MIDI protocol can do, and how to edit the tone of sounds simply, without relying on a complete synthesizer.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I need to decide which language and APIs to use to implement my language, and familiarize myself with the aspects of the language and APIs I will more likely need. This is particularly true for manipulating tone quality. The basic tonematrix could be done with simple MIDI protocol, but control of tonality which I aim to provide probably might need additional power.

**What questions do you have for your critique partners? How can they best help
you?**

I don't have much to ask yet, having not yet leapt down from the idea-cloud into the concrete world, though I have chanced a few glances down and the vertigo has struck. Any feedback or ideas on sane controls for the tonality would be helpful. Should I try to map RGB directly to the qualities of the tone, or should I let users create a tone and store it as a color? The later promises to be too bulky, unless I drastically reduce the ways the tone can be altered, but the former will be very limited and probably less than intuitive. 

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

I put in about 8 hours on the project this week. This was mostly spent working on my conceptual understanding of what I wanted to do and writing the description and plan for the project. This included research on existing DSLs in my domain, and beginning to look into music-APIs in Scala and Java.

## Post-critique summary

## Post-critique reflection
