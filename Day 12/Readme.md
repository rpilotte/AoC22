# Day 12 : Walking and path optimization

For the first time this year, solution "by hand", with 2 eye balls.

Proper solution would have required a proper Dijkstra Search algorithm that can only be achieved with VBA, due to the size of the problem.<BR>
As this seems to be a recurring idea for AoC, I may consider to spend the required amount of time to solve this when I will have some more time.

##Part 1: Walking up the hill

Starting from "E", i.e. the top of the hill, I figured out that the safest was to "spiral" down, slowly, with possible cliff ascension, avoiding to enter dents, as close as possible to this "End point".<BR>
Then, when reaching the plateau of "c" altitude, the trick was to stay, as close as possible to the vertical position of the "S", "Starting" point, avoiding as much as possible to go "down" then "up", or "up then down", avoiding to go "right" at any moment.<BR>
A few "must" "go through" locations have been defined. <BR>
When 2 such points were defined on a same altitude plateau, then regardless of the path, any that is going between them is fine, as long as it stays in the box and keep a steady direction (if down, no up allowed and vice-versa).<BR>

##Part 2; Walking down the hill

That  was very deceptive watching at my height map.

Part 2 is just querying to find the the point where the path found for Part 1 (yes, we walked "downhill" to solev part 1) is reaching to the plateau at altitude "b" that is neighbouring the "a" plateau where the start was located.<BR>
As the first moves are to get through that "uniform" plateau, part 2 just removes all the moves that are in these 2 and then add 2.
My height map, with letters translated from "a"=0 to "z"=25 and with "S"=-1 and "E"=26 is available in the given Excel sheet.

**Happy solving!**
