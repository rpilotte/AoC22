# Day 5

The trick today was to use the "INDEX" function of Excel that returns the content in a specific column/row of an array.<BR>
**AND** to read the instructions<BR>
**AND**, *even more important*, to read the instructions.

In fact, I first forgot to move the crates one by one, causing an inversion in Part 1 and lost crates during this process.<BR>
Then, I figured out that I was not starting with the correct configuration.


## Part 1

For solving this part, 4 steps:
1. Determine the crates that will have to be moved.<BR> 
That's where INDEX comes handy, if piles are column, then the crates to move are at the end of the string that is located in the matching column.<BR>
Some attention is nevertheless needed to ensure that you only move crates that "exist".
2. Invert the order of the crates that are moved.<BR>
For this, the crates letters are extracted one by one, starting from the end into a "crate invertor", then concatenated back, so that the order is inverted<BR>
That's where most of my problems have been lying, my inverter being slightly too small for the maximum number of crates to move.
3. Add the "inverted" list of crates to the correct pile
4. Remove the crates from the correct pile

## Part 2

Here, no need for this stupid inversion, in fact the first solution that I submitted, and only 3 steps are needed as the "inversion" is not.

Happy solving!
