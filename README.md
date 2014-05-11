# Python Sudoku Solver 
A command line python program that finds all solutions for a given initial board.

## How To Use
Enter 81 digits one after the other separated by spaces as command line arguments (0 for empty square) - in row major order. Here's an example run - 

<pre>
$ python sudoku.py 0 0 0 0 0 0 0 1 4 2 0 0 5 0 0 6 0 0 9 0 0 3 0 0 0 0 0 0 5 0 0 1 0 0 3 0 0 8 0 0 3 0 0 7 0 0 6 0 0 2 0 0 9 0 0 0 0 0 0 8 0 0 2 0 0 3 0 0 4 0 0 1 5 7 0 0 0 0 0 0 0
Given board is - 
0   0   0   0   0   0   0   1   4   
2   0   0   5   0   0   6   0   0   
9   0   0   3   0   0   0   0   0   
0   5   0   0   1   0   0   3   0   
0   8   0   0   3   0   0   7   0   
0   6   0   0   2   0   0   9   0   
0   0   0   0   0   8   0   0   2   
0   0   3   0   0   4   0   0   1   
5   7   0   0   0   0   0   0   0   

Solving...

Found solution - 
6   3   5   7   8   2   9   1   4   
2   4   7   5   9   1   6   8   3   
9   1   8   3   4   6   5   2   7   
7   5   2   6   1   9   4   3   8   
1   8   9   4   3   5   2   7   6   
3   6   4   8   2   7   1   9   5   
4   9   6   1   7   8   3   5   2   
8   2   3   9   5   4   7   6   1   
5   7   1   2   6   3   8   4   9   
</pre>

## How It Works
It does a depth-first search of the solution space. At every stage it picks the square on the board with the least number of possible choices and then recursively explores each of them.  

Most sudoku puzzles intended to be solved by humans only have one solution. However it is possible to devise a starting board state that can lead to multiple solutions. The program keeps searching the rest of the solution space for more solutions even after a valid solution is found. 
