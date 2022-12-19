# Day 18: Boiling Boulders

The part 1 is possible with Excel alone. For Part2, Excel over 22 sheets would be needed as the problem is "3D".

##Part 1: Exterior surface of the lava droplet

Each cube that forms the droplet comes initially with 6 faces. Leading to the absolute maximum of exposed faces for the problem.

For Part1, for any pair of cubes that have not been already tested against each other, with both cubes being different ones, if any 2 of the 3 coordinates are the same (for example same X and Y) then 
if the Z values are the same, you have to remove 2 faces in the Z direction (as the cube would basically be a duplicate!)
if the Z values are differing only by 1 (+1, -1), you have to remove again 2 faces in the Z direction as this is a common face that disappear for both blocks.
Do not forget to do the same by testing with same Y and Z coordinates, to remove the faces in the X direction, and by testing with the same Z and X coordinates, to remove the faces in the Y direction.

This can be implemented as a formula in Excel, but the calculation takes "some time".
In VBA, after loading the cubes definition from the table, all the calculations are done without any effect on the table, leading to a very reduced execution time.

##Part 2: Iterating part 1

For part 2, I created a "space", full of "vacuum" (that I considered 0 density) of 22x22x22 and reported the lava cubes inside, as "lava", with a 10000 density.<BR>
I filled (0,0,0), that was "vacuum", with "water" and then propagated the "water" left, right, top, bottom, front and behind, until it was blocked by lava and until no more "water" could be inserted during an iteration.<BR>
In my case this took 4 iterations. 

Once done, I tested 2 approaches:
1. Testing all 22x22x22 locations for them to be "lava". In that case, I was evaluating the number of faces that were exposed to water or at the edge of the proposed space.<BR>
2. From puzzle input, we know the location were to find lava. Testing only on them to find faces exposed to water was the fastest.

There is still a bug in algorithm 1 as it falls too short by 1! 

**Happy solving!**





