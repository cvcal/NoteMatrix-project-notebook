# Design notebook for week ending November 16, 2014

## Description

I finalized many design decisions in my 
[design and implementation](https://github.com/cvcal/NoteMatrixWithTonality/blob/master/documents/design_and_implementation.md) 
document. The parts I've added since last week include clarification on how 
the user will interact with the interface, more direct answers to the 
questions posed in the 
[project description](http://www.cs.hmc.edu/~benw/teaching/cs111_fa14/project.html#description) 
and, going along with this, a more careful consideration of possible incorrect 
inputs. I also continued some research for similar DSLs and programs now that I
have a better idea of what I want to implement.

I have settled on implementing the core of this in Java, though I will keep 
the option of Scala open if part of the project would benefit from the 
different tools that Scala offers. 

Much of the rest of the time I've spent on the project this week was 
productive but doesn't have much to show for itself. For example, setting up 
the project, downloading JMusic and editing class paths as needed to make 
everything (the jmusic jar file and the list of instrument classes) work 
and link up properly. I have been able to link up the .jar as needed, but 
I can't seem to find any way to link up the directory containing the 
instrument classes. I have followed 
[jMusic's instructions](http://explodingart.com/jmusic/GetjMusic.html) 
to the letter, but I am still getting a "SawtoothInst cannot be resolved to a 
type" error. `inst` is directory filled with .java and their compiled .class 
versions, but no way I add this directory to the `CLASSPATH` as specified by 
numerous stack-overflow answers and by 
[the Oracle documentation](https://docs.oracle.com/javase/7/docs/technotes/tools/solaris/classpath.html) 
recognizes this directory's files.

One particular tutorial I might want to keep in mind is the 
[real-time audio](http://explodingart.com/jmusic/jmtutorial/RealtimeAudio.html)
tutorial, but I won't try to worry about that right now.


## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

Right now, I just really need to get the jmusic stuff working, this is getting 
ridiculous. My main design decisions are made, except for a sense of how 
I will specify instruments, so that is still kinda sitting in the waiting room.

**What questions do you have for your critique partners? How can they best help
you?**

Any tips? 

Beyond the jmusic problem, please let me know if any design decisions I've 
made in the 
[design and implementationn](https://github.com/cvcal/NoteMatrixWithTonality/blob/master/documents/design_and_implementation.md) 
page don't make sense, need more clarification, or simply sound less than 
effective for the user.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

About 2 hours on critique and critique reflection. 3.5 hours finishing 
up the design and implementation document. Another 3.5 to 4 hours were spent
trying to set up and debug the jmusic instrument situation. 

## Post-critique summary

Matt pointed out a few things I've been less than clear about, including 
things I've been avoiding. These include the whole "how am I gonna choose the
grid's size" question and details on how to unselect grid squares.

He also suggests I solve the instrument problem by simply including the files
I need into my project, which I think might be the simplest solution as well.

## Post-critique reflection

I asked Prof. Keller about JMusic tips, but he told me his project didn't use 
the JMusic instruments, instead relying only on the midi capabilities and 
built-in Java midi instruments. This, along with in class discussion and 
Matt's comments, convinced me that I should stop trying to fix the problem the 
hard way. I'll include any files I need in my project, properly attributed, and
potentially end up creating my own instruments. Looking at the instrument code
more closely, it might be easier to simply make my own instruments based on the
provided examples, but I'll see if I need this. For now, I'll work to 
implement the basic project structure using existing instruments.

As far as the two problems that Matt identified go, here are my general 
response:
* For inputing the size of the grid, I agree there should be limits. It makes 
  no sense to have a limitless vertical direction, as there are only so many 
  pitches we can generate and hear anyway, so that is naturally limited. A 
  scroll bar might be a nice way to indicate the desired size, that's a pretty 
  elegant suggestion. For the horizontal axis, there's no real reason to limit 
  it, other than the sheer practicality of making looping segments if the 
  contents are too long for the looping to be noticed or well planned out. 
  I'll have to consider that one more carefully. Having scroll bars for both 
  makes sense, but I'll have to consider the limits of the size.
* For unselecting grid squares, the idea is just to click a square that's 
  selected to unselected. If a square has multiple colors, you'd have to be in 
  the color you want to erase, so that clicking a square flips that color's 
  on/off state in that square. It might also be nice to have clear-all option, 
  or a clear-all-of-one-color option.


