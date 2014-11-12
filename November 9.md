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

Paul seemed to be generally positive about the idea, how intuitive the grid
system would be. He suggests a few possible changes or clarifications, which I 
will respond to in the reflection section. 

He had a bit to say about the possibility of having an external DSL to 
store the grid and allow for saving programs, and editing them outside of the 
GUI interface. He confirmed my initial feeling that this might be a nice way
to begin to implement and test the language before worrying about the GUI 
aspect, but also suggested that it would not be as useful as it seems, as users 
of the language would focus on the GUI, and there are other ways to test a GUI.


## Post-critique reflection

First, to answer some of the questions raised by the critique:
* My plan is to not implement the ability to have multiple note-lengths, at 
  least not at first. I will try to implement the grammar in such a way that it 
  would be possible to add different note lengths later without too much 
  difficulty, maybe even actually building that functionality in, but I would 
  focus on implementing the GUI in the simpler way, deferring the added feature 
  to later. If the feature was added, the idea would be to have the user click 
  and drag over multiple box locations to make a single note of that length, as 
  opposed to clicking the boxes individually, which would create separate notes.
  I will be careful to add this type of detail to my design and implementation
  section for Sunday.
* For the possibility of creating your own instrument, that's very technical 
  and largely beyond the scope of the project, I think, but someone with that 
  technical capacity might be able to map a particular color to an instrument 
  that they create by editing the code itself. I'll think of other ways to make
  this possible, but it's gonna be on the back burner for now. Some of the 
  problems involved include the fact that an instrument might just be a
  waveform that's contracted or expanded for the desired frequency, but it 
  often has other variations from one note to another. This is especially 
  across registers, the lower notes of an instrument would have very different 
  overtone patterns, so a tool that just creates a basic waveform would not 
  sound convincingly like its own instrument. Anyway, lots of difficulties with 
  this idea, I think it would be its own project, a language to synthesize 
  sound.
* The grids in parallel shouldn't be necessary, since a single grid can already
  play multiple sounds at the same time. The only problem that might solve 
  would be the possibility of multiple instruments playing the same note at the 
  same time. This is something I'm trying to figure out, but I think I can find 
  cleaner solutions.

I think I will follow the advice for the distinction between implementing the 
sound creation as delayed or real-time. Stick with the delayed solution for 
now, get the rest of the system up and running, and then potentially look into 
finding real-time tools and incorporating those in later, if I continue the 
project past the class.


