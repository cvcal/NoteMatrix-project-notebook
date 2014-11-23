# Design notebook for week ending November 23, 2014

## Description

I spent much of the earlier time this week finding my solution to the 
instrument problem, and subsequently learning things about JMusic and how I can 
do what I want. Things I learned:
* Most midi instruments sound gross (Prof. Keller warned me that the built-in 
  midi instruments in newer versions of Java sound worse than they used to,) 
  but they are really easy to use, and I can use them for prototyping, and can 
  eventually add audio instruments (bypassing the midi suckiness) later, 
  potentially. However, they are nice in that they are super simple since
  you can represent one simply with an integer to represent the value when you
  create a part (series of phrases, which are each series of notes (or 
  CPhrases, which are chords))
  * Some simple midi instruments that don't sound too awful include `Pizz`, 
    `Clavinet`, `Clarinet`, `Bird`, `Panflute`, and `Glockenspiel'.
  * All string instruments sound horrible, and many brass ones do too, 
    of these, the `Fiddle` might be best, if you forget what it's called
* It took me a while to find how to control timing properly, as the JMusic 
  structure just gets you to add a note after a note, without regard to 
  placement, just order. When one finishes, another begins, and you have to 
  explicitly add rests if there shouldn't be a note playing. This means I'll 
  have to leverage phrases to get multiple notes at once, maybe. I'll see how 
  they handle chords first.  
  * [CPhrases](http://explodingart.com/jmusic/jmtutorial/Chords.html), or chord
    phrases, should allow me to have multiple notes at the same time, though I
    will still be keeping each instrument separately in different phrases.

With this newfound knowledge, I've finished the basics of my Grid! 

It works, can play multiple instruments based off of a grid structure, and 
that's cool. I'll have to change a few things in this basic structure if I want
to make loops work (I can't return a score from the Grid, or I can, but I would 
then have to break the score apart and rearrange the pieces a bit to get the 
looping one to work.)

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

My grid works! So now I need to work on my GUI. I haven't really begun to look
into the best ways to do this. If you know of a good place to start looking, 
that would be cool.

**What questions do you have for your critique partners? How can they best help
you?**

I currently have just 6 midi instruments, so I haven't implemented the 
modulation on top of each midi instrument yet. I might do that, or I might work 
to add this extra flexibility after I switch to audio instruments (not midi). 
Is it ok to add the basic GUI first, and the looping functionality, before I 
worry about the extra instruments, or should the focus of my project be more 
about the instruments? 

Also, another question about focus. Should I implement a GUI for what I have 
first, or should I add the looping functionality first. I will have to change 
some underlying structure to get the looping functionality to work properly, 
and I think it might be nicer to do that now, when there isn't a whole other 
set of code that relies on the grid. However, having a working GUI with a 
subset of the functionality will be cool, and that might be more likely to be 
done by the end of the semester if I don't get side-tracked.

Those questions and the GUI question are my basic focuses at the moment.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

I spent about 2 hours on the critique and critique reflection. I then debugged 
(let's admit it, hacked) away my around the build problem I was having: I'm
just going to include the instrument files I decide I need in my project. This 
process took about an hour, making sure everything worked, and I spent another 
hour messing around with the "Make it go Bing" tutorial and the instruments, to
get a better idea of how JMusic works. That's ~4 hours so far. 

I spent some time in class reading JMusic documentation and beginning to build 
the skeleton of my Grid class, so that I have a better idea of what aspects of 
JMusic I need to focus on, what I will need. I also spent a good two to three 
hours more on the tutorials, particularly messing with midi instruments as a 
very simple way to get instruments for a trial version, and began to apply it 
to my grid. That's another ~3-4 hours.

On Sunday, I spent about 3 hours finishing my grid implementation, and an hour
more making my test and adding the repeating functionality, along with 
finishing up my notebook entry.

That's 11-12 hours this week.

## Post-critique summary

## Post-critique reflection
