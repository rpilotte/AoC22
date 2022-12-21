# Day 21: Monkey Math

For Part 1, a small VBA Code is needed to turn the lines into formulas stored in named cells.
For Part 2, during Part 1, I prepared a few values (row of "root" and "humn" and the 2 sides of the "root" calculation) then I used the "Goal Seek" tool, that is standard in Excel, to solve part 2.

##Part 1: performing the calculation

The data structure is very neat: 4 letters as name for the "variable", space, colon, space and then either a number or a formula that is "compatible" with Excel.<BR>
How great!

So let's first split the lines, with "Text to Columns" using ":" as the delimiter

We now need, for every line, to name the cell that is in column 2 with the name in column 1.
1. For this, we extract the name from the first column and the formula, missing the initial "=" from the second one.
2. With a small conversion, we can then create a "range" with the cell in the second column and assign it the extracted name and fill it with the formula, including an initial "=".
3. We take the opportunity of the walk through all the values to save the value for "humn" in a cell that is very accessible and make it a "parameter" that is also very accessible.
4. We also take the opportunity to "split" the line for "root" into its 2 segments and copy them to accessible cells that will be used for part 2.

At the end of the table walk, all is done for part 1, just having to report the value from the cell named "root".

##Part 2: Finding the correct parameter to achieve the balance

Now that "humn" is a parameter and that both parts of the "root" are known and easily accessible, the goal is to ensure that both parts of root are equal.<BR>
For this Excel has an incredible tool: Goal Seeker.

Here the goal is to make the difference between the 2 parts of "root" equal to 0, while changing "humn".<BR>
As all three are now easily accessible, this is just a matter of seconds.
Once run, the answer is stored in "humn" and reported, as expected.
**Happy solving!**
