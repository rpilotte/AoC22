# Day 15: Beacon Exclusion Zone

A nice problem today.
Hopefully, I already used "Taxidistance" aka "Manhattan distance" in the past.

Part 1 was mostly solved "manually" but knowing part 2 would have been "immediate".
Part 2 is very challenging from an algorithmic point of view!

##Part 1: Determine and validate the proper mechanisms to calculate the "segments" at a given Y value

As said some manual activities to solve part 1, not knowing part 2.
For solving it, knowing part 2, its close to immediate, unless you are not lucky!
Then remove 1 and you are done ;-) 

##Part 2: Iterating part 1

Here, no possibility to escape automatic segment reconciliation!!

For this I decided to sort the segments that were created by the 28 beacons at a given Y value first according to segment start and then according to segment end.<BR>
This is needed to speed-up the calculations as this allows to ensure that the segments that are existing are grouped together.<BR>
Starting from the segment with the highest "end value", so 4000000, its beginning is then the good point to start from.<BR>
You then have to compared the end of the next highest segment with the beginning of the segment that is growing at the end of the line.

The segment is falling short? You found your "hole"!

The Excel VBA proved to be with acceptable performances, about as good as non compiled Python 3!

**Happy solving!**
