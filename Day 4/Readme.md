# Day 4

The trick today was to use basic geometric properties to calculate some intersections and their length.<BR>
The below only works if the segments are defined by values that are ordered: for segment A-B, this means that A<=B!

## Part 1

A segment A-B is fully included in another, C-D, it A<=C *and* B>=D/.<BR>
The trick is that for this puzzle, one has also to test that C-D can also be included in A-B.<BR>
As both condition are leading to meet the criteria, a "*OR*" is needed between the two tests base tests.

For line 1, and with segment letter corresponding to columns, the above immediately translate to Excel `=IF(OR(AND(A1<=C1,B1>=D1),AND(A1>=C1,B1<=D1)),1,0)`, where 1 means that one of the segment is fully included in the other.<BR>
What is left to solve the puzzle is to sum on all 1000 lines of the puzzle.

## Part 2

Considering that A<=B and C<=D, segments overlap if MAX(A,C) is less than the MIN(B,D).<BR>
This is easy to understand: the end of the segment that starts the latest must be less than or equal to the beginning of the segment that starts the first.

Again, under the same assumption as for part 1, the above formula also immediately translates to Excel as `=IF(MAX(A1,C1)<=MIN(B1,D1),1,0)` and
what is left to solve the puzzle is to sum on all 1000 lines of the puzzle.

Happy solving!
