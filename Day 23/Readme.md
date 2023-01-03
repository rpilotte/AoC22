# Day 23: Unstable Diffusion

Some decided to go with a grid with a big offset...
With Excel, only with formulas, that would have been cumbersome, so this is, again, a full VBA solution.

I went the route of defining an Elf as a new VBA type with X and Y, its current coordinates, starting from 1 on top left part of the given input, and with proposal values for the same coordinates.

I then wrote a procedure (a subroutine in VBA's syntax) to "create" the table that contains all the elfs, as per the given input.<BR>
An "#", or an elf, at 60th position (first char is position 1) of line 5, gets X=5 and Y=60.

Another useful boolean function has then been created to find if an elf is occupying a specific position.<BR>
This is useful to check if there are elfs at N,NE,E,SE,S,SW,W and NW positions.<BR>
If an elf is present at the given position, it returns true, else, it returns false.

I also created another function that return if at least one other elf has proposed to move to a given position.<BR>
This is basically the same as the above one, but on the proposal rather than on the current values.<BR>
Quite handy to check if an elf can move, or not to its new position.

Last but not least, a subroutine (mostly called a procedure in many other languages), has been created to reset the proposals between two rounds.


##Part 1: Getting the total space after 10 rounds

Using above functions, a resolution subroutine has been created to 
1. Test that a specific elf has no neighbours all around or in the given directions.
2. Based on the above, and depending on the set of instructions for that specific round, proposal for that elf were created.
3. Proposals are then evaluated and if not other elf is proposing to the same point, the move is made and logged (this is useful for part 2).<BR>
If the positions are colliding, the move is cancelled.
4. Proposals are reset so that a next round can be performed.
5. After 10 rounds, the rectangle that contains the elfs is calculated based on the min and max values for X and Y coordinates of the complete set of elfs.<BR>

Solution for part 1 is simply (Max X - Min X + 1) * (Max Y - Min Y + 1) - Number of elfs

With Excel, on a recent MacBook Pro with Intel Core i7 at 2.3 GHz, this already took more than 1 minute.
 
##Part 2: Getting all elfs alone

For part 2, you keep on iterating and that's were the logging added at step 3 comes handy.
You just end as soon as there are no moves happening.

With Excel, on a recent MacBook Pro with Intel Core i7 at 2.3 GHz, this took several hours as 10 steps are already about 2 minutes and more than 900 steps were to go.

**Happy solving!**
