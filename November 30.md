# Design notebook for week ending November 30, 2014

## Description

This was thanksgiving week. I didn't do much. I did edit the 
[evaluation ](https://github.com/cvcal/NoteMatrixWithTonality/blob/master/documents/evaluation.md) 
document, talk with Sisi in class about designing the interface to be usable 
and intuitive, and read Mauricio's critique.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I need to work on my GUI, I haven't done much on it yet, but I'll look at
the resources that Mauricio recommends.


**What questions do you have for your critique partners? How can they best help
you?**

I'm not sure. I'd appreciate feedback on how best to aid the user in 
'eyeballing' the intervals. I think some markers are useful, but should 
they consist of actual letter names (ABC or DoReMi) along the rows, or simply 
having some rows be highlighted. Should the user be able to specify which 
highlights to have, and if so, can they shift those to correspond with the 
fundamental of the scale they are messing around in?

For example, this is necessary to prevent having to count to 12 every time you
want an octave.

**How much time did you spend on the project this week? **

About 3.5 hours. 2 of those on the evaluation, another hour talking with Sisi 
and subsequent deliberation about the best way to aid interval recognition.
The rest of the time spent editing this and last week's notebook in response
to the critique and stuff.

## Post-critique summary

Paul seemed to like where the project had gone, but wanted to see more testing
for the backend. He also suggested considering a minimally-viable GUI to start
with, and to add to it incrementally, to maximize the chance of having something
working by the end. He also suggests I make it easier to download the project.  

## Post-critique reflection

I agree with pretty much everything Paul said. I need to prioritize my goal 
though. I will put off making the language easy to install/download until I 
actually know what I need for it. I can probably still improve the current 
process though, for people who want to download the code.

For testing, I definitely should look into it. Currently, I haven't really done 
anything because there is frankly so little to test. The backend is more of a 
it-works/it-doesn't situation, at least for now, and I don't know much about how 
to compare midi files to see if they are what they should be. I will continue 
making examples and testing by hand, but I probably won't make an extended suite 
of tests for a little bit, I think my priority should be on getting the language 
to actually be interfaced properly - aka graphically.

For the GUI, I have been considering a minimally-viable option: I need a grid
that makes notes, a color-selector to make the right notes, and a "play"
button. Extentions include : making it pretty, having the intervals highlighted 
as I described above, and adding the looping, or at least being able to specify
how often to loop the current grid.
