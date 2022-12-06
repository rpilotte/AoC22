# Day 6

The trick today was to use "fake" data to automate as much as possible the check for strings with all different characters.<BR>
As all the chars where from "a" to "z", I used "random" chars to "prefix" a sequence to test.<BR>
The idea is that a given sequence of n char is with all different chars if all of the n sequences that starts at position 1\<=i\<=n and prefixed with the above "random" are having chars that are differing to respectively each of the previous n chars.

## Part 1

For part 1, as only 4 chars, this can be done with a simple "if" test, considering that you want to test that a string located at A1 has 4 consecutive unique chars starting at position given by cell B2:<BR>
`=IF(AND(MID($A$1,B$2,1)<>MID($A$1,B$2+1,1),MID($A$1,B$2,1)<>MID($A$1,B$2+2,1),MID($A$1,B$2,1)<>MID($A$1,B$2+2,1),MID($A$1,B$2+1,1)<>MID($A$1,B$2+2,1),MID($A$1,B$2+1,1)<>MID($A$1,B$2+3,1),MID($A$1,B$2+3,1)<>MID($A$1,B$2+2,1)),1,0) `<BR>
If you have an index in line 2, that increases by 1 from column to column, the above formula can be expanded to scan the whole chain.

What is left is to find the first occurence in the generate data.<BR>
For this Excel has a tool called "Conditional Formating" that allows to highlight specific values in the table.<BR>
My personal "trick" is to copy the results and paste them in a new row "as Values". A simple "find" for `1` on that single row brings you to the first occurence ;-) 

## Part 2

This is where the "random" chars come handy as for the first char, the result of checking that it is all different to the 13 previous will always return "true" or `1`.<BR>
If second char is same as first, then checking with the 14 previous will return "false", else, it will return "true", and so on...

Then one has to check that this is "true" for all 14 tests.

Neat and clear.

Happy solving!
