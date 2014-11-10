# Design notebook for week ending November 9, 2014

## Description

Quick list of resources I've been using, and questions that have arisen from this reading.

* I watched some of Mark Lewis' intro videos on making GUI stuff in Scala ([he makes a quick "game" that shows a lot of the basic controls and API calls](https://www.youtube.com/watch?v=AIdBBMVrRLQ)), to get an idea of what is easy or hard to do. I found his videos after looking for examples of using Java libraries in Scala, to see if there would be any difficulty using JMusic, which I am currently leaning towards as a sound creation library to use.
* I re-read up on sbt stuff, to actually learn the tool, and be able to setup my directory structure, dependencies, and things, so I spent a significant chunk of time on [the sbt page's tutorials](http://www.scala-sbt.org/0.13/tutorial/).
* I've been reading more about JMusic, looking through the [tutorials](http://explodingart.com/jmusic/jmtutorial/t1.html)
  * Some possible issues include the fact that JMusic, while powerful, is [NOT meant to be a real-time compositional tool](http://explodingart.com/jmusic/jmtutorial/x22.html). This means it will work great if what I want to do is let users map out their song, then click a "play" button, at which point the language can "compile" and produce some audio file, which the GUI could play, potentially, but it might not work if I want my final product to be as immediate and intuitive as tonematrix.
  * Some nice things about JMusic include the sheer quantity of instruments and synths I could work from for the different tone quality options I want to provide. Turns out making instruments is hard?

In an effort to clarify my thought process and my vision for this project, I made some nice images.
* This is the basic idea, the first image with notes, and the second with some squares colored in for a feel of what it would look like with things being pressed.
	 \centerline{\includegraphics[height=3in]{https://github.com/cvcal/NoteMatrixWithTonality/blob/master/documents/initial_examples/GUI_idea_simpleWithNotes.png}}
	 ![Basic with notes](https://github.com/cvcal/NoteMatrixWithTonality/blob/master/documents/initial_examples/GUI_idea_simpleWithNotes.png)
	![Basic in use](https://github.com/cvcal/NoteMatrixWithTonality/blob/master/documents/initial_examples/GUI_simple_inUse.png?raw=true)
* This is that idea, with the possibility of having a single not last more that one beat. 
	![Multiple beats](https://github.com/cvcal/NoteMatrixWithTonality/blob/master/documents/initial_examples/GUI_idea_continuousTime_inUse.png?raw=true)
* This is the original idea with the addition of being able to loop multiple grids a preset number of times 
	![Loops](https://github.com/cvcal/NoteMatrixWithTonality/blob/master/documents/initial_examples/GUI_idea_withLoops_inUse.png?raw=true)

I think that I want the user / programmer to go through the following order for each composition, regardless of whether coding in text (in the intermediate representation) or when using the GUI (if that gets implemented and works). I think this will help both me, in terms that it will set a number of things in stone and make the rest of the process more straightforward.


## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?** AND **What questions do 
you have for your critique partners? How can they best help you?**

I would appreciate input on that third bullet up above. Should I be ok with a delay in the compilation of a program and the creation of sound, or should I aim for a real-time composition tool?

The real-time aspect does make it feel less like a language, though there would still be some form of IR, but it would force me to focus on the GUI from the start, which I'm thinking is counter to the learning-objective that Prof. Ben has for this project.

I'm leaning towards the 'press play' approach, as that feels more straightforward, both in terms of the library I can use, and in terms of implementing things like the looping feature, but that does break the immediacy of the initial idea, and would make the language slightly less intuitive. It's a pretty fundamental question with points on both sides, so I'd like someone else's opinion.


**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

## Post-critique summary

## Post-critique reflection
