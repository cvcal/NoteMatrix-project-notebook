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
  <img src="https://github.com/cvcal/NoteMatrixWithTonality/blob/master/documents/pictures/multipleColorCells.png" width="200" />
</p>

I have started to transfer this to my grid, and hacked together a starting version of [Tonatrix](https://github.com/cvcal/NoteMatrixWithTonality/blob/master/src/main/Tonatrix.java) 
that basically creates the grid from BasicGridTest, then displays this generated 
grid on the GUI. The GUI does not yet have the clicking interface implemented, as 
I have yet to get to it, but I added the hack that clicking plays the grid, so you 
see the code-generated grid, and can click on it to hear it play. Also, the 
coloring of cells when they are selected by multiple instruments at once does not seem 
to be working yet, I need to debug this. This is what the trial looks like:

<p align="center">
  <img src="https://github.com/cvcal/NoteMatrixWithTonality/blob/master/documents/pictures/initialGrid-alpha.png" width="150" />
</p>


## Questions

**What is the most pressing issue for your project? What design decision do you need to make, what implementation issue are you trying to solve, or how are you evaluating your design and implementation?**

For transferring the GUI stuff to my musical grid, I need to choose how best to 
represent certain things. I should porbably keep the backend and GUI things in 
the same class, but this means I need to be careful with how they overlap. 

I also need to figure out the best way to add the color-selection grid. Should 
this also be in the same Grid class? I think this is the point where I might be 
making the Grid class do more than it should, but if it isn't there, then 
I'm going to need a ton of message passing.

**What questions do you have for your critique partners? How can they best help you?**

Any opinion on the best way to separate GUI from backend would be welcome. 
Advantages of keeping them together include having access to all the boundary-
condition definitions directly, instead of having to pass checks around, but then 
I have the problem of the color-picker needing to be somewhere, and needing to 
keep the state of "selected color" for the Grid to know what a click to a grid 
cell means. 

I also haven't learned how to best lay the different GUI components out on the 
JFrame.

**How much time did you spend on the project this week?**

I spent a good 2-3 hours on the critique this week (in the 3+ range if you 
count inclass time, 2+ without).

I spent 6-ish hours on the tutorials and making the grid example on Saturday. 
Another quick hour editing this and adding the 3- and 4-color split in the grid
example on Sunday.

Add 3 hour of critique reflection and adding functionality to my actual grid
later on Sunday.

Total of 12-13 hours.


## Post-critique summary

## Post-critique reflection
