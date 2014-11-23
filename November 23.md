# Design notebook for week ending November 23, 2014

## Description

I spent much of the earlier time this week finding my solution to the 
instrument problem, and subsequently learning things about JMusic and how I can 
do what I want. Things I learned:
* Most midi instruments sound gross (Prof. Keller warned me that the built-in 
  midi instruments in newer versions of Java sound worse than they used to,) 
  but they are really easy to use, and I can use them for prototyping, and can 
  eventually add things later, potentially.
* It took me a while to find how to control timing properly, as the JMusic 
  structure just gets you to add a note after a note, without regard to 
  placement, just order. When one finishes, another begins, and you have to 
  explicitly add rests if there shouldn't be a note playing. This means I'll 
  have to leverage phrases to get multiple notes at once, maybe. I'll see how 
  they handle chords first.  

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

**What questions do you have for your critique partners? How can they best help
you?**

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

I spent about 2 hours on the critique and critique reflection. I then debugged 
(let's admit it, hacked) away my around the build problem I was having: I'm
just going to include the instrument files I decide I need in my project. This 
process took about an hour, making sure everything worked, and I spent another 
hour messing around with the "Make it go Bing" tutorial and the instruments, to
get a better idea of how JMusic works. That's ~4 hours so far. I spent some 
time in class reading JMusic documentation and beginning to build the skeleton
of my Grid class, so that I have a better idea of what aspects of JMusic I need 
to focus on, what I will need.

## Post-critique summary

## Post-critique reflection
