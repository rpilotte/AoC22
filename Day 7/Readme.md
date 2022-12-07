# Day 7

A lot of string parsing and conditions needed to re-create the full path names to files and directories.<BR>
Once done, going through the directory walk to create the hierarchical table of directory sizes, based on their depth.

The lesson of the day:<BR>
**Don't try to have a nice solution from a visual point of view: `0` are acceptable values **

# Part 1

You have then to filter on the directories that are smaller than the requested value, and sum all values in that filtered table.<BR>
Et voilà!

## Part 2

Just reusing the hierarchical table of directory sizes, sorted them and then removed the minimun size to be freed.<BR>
To things easy, consider only to present the values that would match.<BR>
A last calculation to find the minimum value on this last table and part 2 is solved!


Neat and clear.

Happy solving!
