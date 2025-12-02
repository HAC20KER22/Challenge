# Challenge

2435. Paths in Matrix Whose Sum Is Divisible by K

My first attempt at solving this problem used a simple recursive DFS approach where I explored every possible path from the start to the bottom-right cell, carrying the sum along with me. While this solution was straightforward and easy to reason about, it had exponential time complexity and quickly became too slow for larger grids. I then recognized that the problem required dynamic programming to efficiently reuse computed results rather than recalculating repeated subpaths.

In my optimized solution, I implemented a bottom-up DP that tracks, for each cell, how many ways we can reach it with each possible remainder modulo k. This allowed me to combine results from the top and left cells without recomputation, reducing the runtime from exponential to polynomial. By only storing DP data for the current and previous row, I also minimized memory usage. The final version runs efficiently even on large inputs and passes all constraints.
