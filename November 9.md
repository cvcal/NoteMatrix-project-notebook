# Design notebook for week ending November 9, 2014

## Description

Quick list of resources I've been using, and questions that have arisen from this reading.

* I watched some of Mark Lewis' intro videos on making GUI stuff in Scala 
  ([he makes a quick "game" that shows a lot of the basic controls and API calls](https://www.youtube.com/watch?v=AIdBBMVrRLQ)), 
  to get an idea of what is easy or hard to do. I found his videos after 
  looking for examples of using Java libraries in Scala, to see if there would 
  be any difficulty using JMusic, which I am currently leaning towards as a 
  sound creation library to use.
* I re-read up on sbt stuff, to actually learn the tool, and be able to setup 
  my directory structure, dependencies, and things, so I spent a significant 
  chunk of time on [the sbt page's tutorials](http://www.scala-sbt.org/0.13/tutorial/).
* I've been reading more about JMusic, looking through the 
  [tutorials](http://explodingart.com/jmusic/jmtutorial/t1.html)
  * Some possible issues include the fact that JMusic, while powerful, is 
    [NOT meant to be a real-time compositional tool](http://explodingart.com/jmusic/jmtutorial/x22.html). 
    This means it will work great if what I want to do is let users map out 
    their song, then click a "play" button, at which point the language can 
    "compile" and produce some audio file, which the GUI could play, 
    potentially, but it might not work if I want my final product to be as 
    immediate and intuitive as tonematrix.
  * Some nice things about JMusic include the sheer quantity of instruments 
    and synths I could work from for the different tone quality options I want 
    to provide. Turns out making instruments is hard?

In an effort to clarify my thought process and my vision for this project, I 
made some nice images, and have started working on the [design and implementation](https://github.com/cvcal/NoteMatrixWithTonality/blob/master/documents/design_and_implementation.md) 
document with some more detailed description of what I want with the final 
product, and how this will impact and help determine implementation.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?** AND **What questions do 
you have for your critique partners? How can they best help you?**

I would appreciate input on that third bullet up above. Should I be ok with a 
delay in the compilation of a program and the creation of sound, or should I 
aim for a real-time composition tool?

The real-time aspect does make it feel less like a language, though there 
would still be some form of IR, but it would force me to focus on the GUI from 
the start, which I'm thinking is counter to the learning-objective that Prof. 
Ben has for this project.

I'm leaning towards the 'press play' approach, as that feels more 
straightforward, both in terms of the library I can use, and in terms of 
implementing things like the looping feature, but that does break the 
immediacy of the initial idea, and would make the language slightly less 
intuitive. It's a pretty fundamental question with points on both sides, so 
I'd like someone else's opinion, to make sure I'm not making a mistake.

Another question I have is whether I should use Scala or Java. I realize that 
they are essentially exchangeable for many things, and they can use the same 
APIs, but Scala would allow me to make a nicer intermediate representation 
syntax, and Java might be slightly more accessible / broadly supported. Is 
this even true? I know Scala can be run anywhere the Java VM is, but I feel 
like Java might still be easier to share with people.


**How much time did you spend on the project this week?**
Counting critique, critique reflection, and everything, somewhere between 8 
and 9 hours.


## Post-critique summary

## Post-critique reflection
