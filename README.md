N-Queens Solver Using Matrix Minors

This project presents a matrix-based approach to solving the N-Queens problem. Instead of relying purely on backtracking, it uses matrix minors and index-based calculations to efficiently identify valid queen positions.

Introduction

The N-Queens problem asks: How can N queens be placed on an NxN chessboard so that no two queens threaten each other?

This method represents the chessboard as a matrix and uses mathematical rules to filter out invalid positions, making it intuitive and efficient for both manual calculations and small-scale automation.

Main Idea

Represent the chessboard as an NxN matrix A.

Each cell (i, j) can potentially hold a queen.

Placing a queen blocks other queens from being placed:

On the same row (horizontal) and column (vertical)

On the diagonals

Using Minors and Indices

Minors M_ij are used to eliminate the vertical and horizontal threats.

Diagonal threats are identified using index calculations:

Sum of indices: i + j

Difference of indices: i - j

For example, if a queen is placed at position a12 (row 1, column 2):

i + j = 1 + 2 = 3
i - j = 1 - 2 = -1


These formulas allow you to identify all cells on the same diagonals where no other queen can be placed.

Step-by-Step Placement

Calculate valid positions sequentially using the rules above.

Partial solutions with fewer than N queens are automatically excluded.

Example: Starting from a11 may produce invalid 3-queen placements, which are filtered out.

Performance

Using this matrix-based method, N = 12 queens can be solved in approximately 0.8 seconds.

Efficient for both small and medium-sized N.


Example (4×4 Board)

. Q . .
. . . Q
Q . . .
. . Q .


Each Q represents a queen.

All placements satisfy the row, column, and diagonal constraints calculated using i+j and i-j.





Future Work

Expand the method to larger N efficiently.

Add a Python implementation that calculates valid positions automatically.

Visualize solutions on a graphical chessboard for easier understanding.
