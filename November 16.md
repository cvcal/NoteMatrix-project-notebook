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
[design and implemenation](https://github.com/cvcal/NoteMatrixWithTonality/blob/master/documents/design_and_implementation.md) 
page don't make sense, need more clarification, or simply sound less than 
effective for the user.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

About 2 hours on critique and critique reflection. 3.5 hours finishing 
up the design and implementation document. Another 3.5 to 4 hours were spent
trying to set up and debug the jmusic instrument situation. 

## Post-critique summary

## Post-critique reflection
