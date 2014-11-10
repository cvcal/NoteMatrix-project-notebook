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

### Here are some things I've been looking at:

Generally reading up on what [MIDI](http://www.midi.org/index.php) is, what it can do, and how.

#### Music APIs
* [jMusic](http://explodingart.com/jmusic/) is huge, it's what Prof. Keller uses for Impro-Visor.
* [JFugue](http://www.jfugue.org/index.html) probably could get the work done, but goes to far down the [abcnotation](http://abcnotation.com/) path for my liking. It does have support for different types of sounds, I'll have to look more into how it allows manipulation of this. Apparently it supports microtonal stuff, which is cool.
* Scala seems to have less developed libraries, which makes sense. [scala-midi](https://code.google.com/p/scala-midi/) is a thing.

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

I feel that quite a bit of Mauricio's criticism was centered around two main points: First, he thinks I should make something that *isn't* the same as tonematrix, adding features to add to the realm of what is possible, and to make the feel of using the language different. Second, he expressed some concern over the primary focus of my project, and whether I would spend enough time on the design and language aspect, instead of getting distracted by the GUI. 

Concerning the first of these two points, Mauricio suggested a number of features and tools that he thought of while playing around with tonematrix. 

## Post-critique reflection
From these comments I learned a few things. First, some of the suggested features were replicating the tools I was suggesting, but did so in a different way. Aside from the obvious "yes, there are many ways to implement an interface for making a note longer," as one example, it made me realize that I hadn't been sufficiently clear in my own description, and that many of the terms that made sense to me, in my mind, were not necessarily clear to people living outside of my skull. I know, shocker, right?

This lead me to discuss my idea with Mauricio, in person, during class on Wednesday. I realized where some of the confusion lay, and decided to make some nice images to better describe what my overall vision was. I also got to ask some followup questions. I asked if he had any opinion the type of scale I should use for my pitch axis, whether I should have the entire chromatic scale and allow the users all western harmonies, or whether I should limit the choice in the hope of keeping the language easier to use. I also asked, and this time with a pencil to draw out some different ideas, how to ask the user to input the color. This process really did help identify some problems with a number of methods I was thinking about.


