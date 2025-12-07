N-Queens Solver Using Matrix Minors

This project presents a matrix-based approach to solving the N-Queens problem. Instead of relying purely on backtracking, it uses minors and index-based calculations to identify valid queen positions efficiently.

Main Idea

Represent the chessboard as an NxN matrix 
𝐴
A.

Each cell 
(
𝑖
,
𝑗
)
(i,j) can potentially hold a queen.

Placing a queen blocks other queens from being placed:

On the same row (horizontal) and column (vertical)

On the diagonals

Using Minors and Indices

Minors 
𝑀
𝑖
𝑗
M
ij
	​

 are used to eliminate the vertical and horizontal threats.

Diagonal threats are identified using:

Sum of indices: 
𝑖
+
𝑗
i+j

Difference of indices: 
𝑖
−
𝑗
i−j

For example, if a queen is placed at position a12 (row 1, column 2):

𝑖
+
𝑗
=
1
+
2
=
3
i+j=1+2=3

𝑖
−
𝑗
=
1
−
2
=
−
1
i−j=1−2=−1

These calculations identify all cells on the same diagonals where no other queen can be placed.

Step-by-Step Placement

The method allows manual or algorithmic calculation of valid positions sequentially.

Ensures partial solutions with fewer than N queens are excluded automatically.

Example: Starting from a11 may produce invalid 3-queen placements, which are filtered out.

Performance

Using this matrix-based method, N = 12 queens can be solved in approximately 0.8 seconds.

Efficient for both small and medium-sized N.
