# Day 3

The trick today was to count the number of occurrences of a specific letter in a string.<BR>
For this, as Excel is a little tricky, the idea is to substitute the requested letter by "nothing", i.e. "", and count the difference between the length of the original string and of the modified one.

To count the "a"s in cell A1, use
`
=LEN(A1)-LEN(SUBSTITUTE(A1,"a",""))
`
A value > 0 means that the character is present in the string.

## Part 1
=======

Using the above, first is to split the input string into 2 parts of same length.<BR>
This is easy using the "LEN\(\)", "LEFT\(\)" and "RIGHT\(\)" functions.

Considering that you have to split cell A3 of even length, the two following formulas can be used
`
=LEFT(A3,LEN(A3)/2)
=RIGHT(A3,LEN(A3)/2)
`
Typically LEFT would go to B3 and RIGHT to C3, or vice-versa, who cares ;-)

Then create a table with all 52 letters and their associated priorities in two rows, and as separated columns, starting from D1.<BR>
I my case, letters are row 2 and priorities are row 1.

You can then test each of the 52 letters on both strings and, if the letter is present in both, return its priority, else return 0 or "".

To get the puzzle answer, just sum all priorities over the whole created table.

In my proposed solution, note that creating the LEFT and RIGHT strings can be skipped and that this can be added in the already "long" formula for testing each letter in each input string.<BR>
Defining them is nevertheless useful as it avoids having to split the same string 104 times (52 for RIGHT and 52 for LEFT).<BR>
On modern infrastructures, CPU is likely not as an issue as memory may be, but it is worth to note that there might be some "optimisation" paths.

## Part 2
=======

No need to split here, just to manage blocks of 3 rucksacks.<BR>
For this, a simple formula to create a numbering scheme that goes 123123...<BR>
To create A2 from A1 that is either a value or empty (read \"\"), you can use
`
=if(A1<3,A1+1,1)
`

You can then test on this value to be 1 while iterating across the lines of the problem to check that this line and the following two are sharing a letter/priority, as for Part 1.

Again, to get the puzzle answer, just sum all priorities over the whole created table.


Happy solving!
