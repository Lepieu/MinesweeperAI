# MinesweeperAI

This is an AI algorithm designed to be able to beat an 8x8 version of Minesweeper (most of the time). This program was made in Python, and it was submitted to the Harvard CS50 AI course. 
It works by making inferences about which of the surrounding tiles are safe using 3 rules:
   
NOTE: The notation is X = {a, b, c}, where X is mines surrounding x, and {} is the set of unknown (moveable) surrounding tiles

1. If a tile has 0 surrounding mines or all surrounding mines are known, the rest of the tiles are marked/ as safe
2. If X = {a, b, c, ...} where the set contains X tiles (or a length of X), all tiles are marked as mines
3. If X = {a, b, c}, Y = {a, b, c, d, e}, an inference is made that X-Y = {d, e}

## How to Use

After launching, you can either make your own move or have the AI move for you. On the first move, the AI will always pick the top left square, so it is advised to pick the first move yourself
The AI will try to make a move using tiles it knows are safe, and if none are available, it picks a tile that is not already known to be a mine. 

NOTE: The AI's "last resort" option picks the top-left most tile instead of randomly picking a tile (This was because I didn't have a list of all possible moves, so it would have had to iterate through every tile a random amount of times, which could cause it to take a really long time to select a mine sometimes)
