# Design notebook for week ending December 7, 2014

## Description

Much of this week was spent learning about GUI stuff, it's been a while since 
I've last had to code event listeners, so I needed to brush up. I first tried 
getting used to Swing, then tried objectdraw at Mauricio's suggestion, but 
found that it wouldn't be capable of doing everything I need, it *is* intended 
as just a teaching tool.

The most useful/applicable example I did is in 
[CoreControl.java](https://github.com/cvcal/NoteMatrixWithTonality/blob/master/src/tutorials/Swing/CoreControl.java).
It's based originally off of a question on stackoverflow, and I then edited 
some aspects to practice mouse event handling in a way relevant to my project:
when you click a cell in CoreControl's grid, it turns red! 

I then extended this to make it more complex/add more of the functionality I'm 
interested in having in my GUI, by allowing multiple clicks to paint the 
grid's cell into different colors, spliting the cell into sub-polygons each 
with a color. It colors the cells with 1, 2, 3, or 4 colors based on the number
of tims each cell was clicked.
[GridTrial.java](https://github.com/cvcal/NoteMatrixWithTonality/blob/master/src/tutorials/Swing/GridTrial.java).
Here's what itlooks like:

<p align="center">
  <img src="https://github.com/cvcal/NoteMatrixWithTonality/blob/master/documents/pictures/multipleColorCells.png" width="250" />
</p>

I think transferring this to the actual grid I'm interested in should be much more doable now that I'm more comfortable with how to approach the problem.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

**What questions do you have for your critique partners? How can they best help
you?**

**How much time did you spend on the project this week?**

I spent a good 2-3 hours on the critique this week (in the 3+ range if you 
count inclass time, 2+ without).

I spent 6-ish hours on the tutorials and making the grid example on Saturday. 



## Post-critique summary

## Post-critique reflection
