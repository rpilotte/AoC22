# Day 2
Two solutions in Excel for this morning!
The real challenge this morning has been to figure out the correct resulting values for each game, from the lengthy instructions.
I finally figured out, after a few tests, that the outcome of any of the 9 possibilities would always the the same, regardless when it is happening.
## Part 1
The table reads as 
| Input | Description | Explanation | Value
| ----------- | ----------- | ----------- | ----------- 
| A X | You play Rock, he plays Rock| This is a Draw=3, and you have 1 for Rock| 4
| A Y | You play Paper, he plays Rock| You win=6, and you have 2 for Paper| 8
| A Z | You play Scissors, he plays Rock| You lose=0, and you have 3 for Scissors| 3
| B X | You play Rock, he plays Paper| You lose=0, and you have 1 for Rock| 1
| B Y | You play Paper, he plays Paper| This is a Draw=3, and you have 2 for Paper| 5
| B Z | You play Scissors, he plays Paper| You win=6, and you have 3 for Scissors| 9
| C X | You play Rock, he plays Scissors| You win=6, and you have 1 for Rock| 7
| C Y | You play Paper, he plays Scissors| You lose=0, and you have 2 for Paper| 2
| C Z | You play Scissors, he plays Scissors| This is a Draw=3, and you have 3 for Scissors| 6
## Part 2
The table reads as 
| Input | Description | Explanation | Value
| ----------- | ----------- | ----------- | ----------- 
| A X | He plays Rock, and you need to lose, so you play Scissors.| You lose, and you have 3 for Scissors| 3
| A Y | He plays Rock, and this needs to be a draw, so you play  Rock| This is a Draw=3, and you have 1 for Rock| 4
| A Z | He plays Rock, and you need to win, so you play  Paper| You win=6, and you have 2 for Paper| 8
| B X | He plays Paper, and you need to lose, so you play  Rocks| You loose=0, and you have 1 for Rock| 1
| B Y | He plays Paper, and this needs to be a draw, so you play  Paper| This is a Draw=3, and you have 2 for Paper| 5
| B Z | He plays Paper, and you need to win, so you play  Scissors| You win=6, and you have 3 for Scissors| 9
| C X | He plays Scissors, and you need to lose, so you play  Paper| You lose=0, and you have 2 for paper| 2
| C Y | He plays Scissors, and this needs to be a draw, so you play  Scissors| This is a Draw=3, and you have 3 for Scissors| 6
| C Z | He plays Scissors, and you need to win, so you play  Rock| You win=6, and you have 1 for Rock| 7

## Implementation in Excel
Two possibilities here:
- Brute force with long "if" tests
- Lookup tables, based on the above ones, just keeping the first and last columns

## Interesting finding
Have you noticed that each combination comes with a different value between 1 and 9?

No magic here, as a lose is 0, a draw is 3 and a win is 6, considering that the 3 elements are valued from 1 to 3.

Value of the object = 1 + ternary value as low trit.

Outcome of the game = ternary value as high trit.

Ternary arithmetic would have been great here ;-)


*Happy solving!*