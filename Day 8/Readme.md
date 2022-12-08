# Day 7 : Finding the trees!

The most difficult part today has been to get the data to Excel.<BR>
Excel was importing the values as numeric values.<BR>
I had to "pre-process" the data before importing them.

Then it has been about 
- Parsing the lines to "individual trees", in a bi-dimensional array
- Finding the correct strategy to mark the border of the created array

For Part 1, it was possible to find a solution only with Excel Formulas, but this was impossible for Part 2!<BR>
###Part 2 required the first VBA code of the season

## Part 1

The idea was to have additional "trees" of negative value (-1) around the array of proposed values.<BR>
Once done, if a "tree" is taller (read is strictly larger) than any of the ones in a direction (read the maximum size in that direction), then it is an elegible candidate.<BR>
Remember, again, a "tree" can be visible from many direction and should only be counted once.

## Part 2

A little bit more tricky as there are searches and calculations to be done, in all 4 directions.<BR>
The only way was to write some VBA code, considering the exact configuration of my tables.<BR>
That required some offsets in some directions.<BR>
As here the goal is to find the longest distance to a tree that is of the same size, or higher, the additional "trees" that we added for part 1 have been turned to higher ones, of size 10, strictly higher than any trees on the map.<BR>
But that brought a problem, as those "fake" trees should not be counted. The distance to get to such a tree has to be reduced by 1.
The scenic score in a given direction is then the distance + 1.
The process is performed in all 4 directions and the values are multiplied together.
In order to speed up the process for the trees at the edges, tests have been added to stop the walk process in another direction is we are at the edge.<BR>

A VBA code has been created to create the table of the Scenic Score for each tree.

Happy solving!
