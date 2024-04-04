---
layout: post
title: 2021-2 Discrete Mathematics 
subtitle: Coding Assignments
tags: [Bachelor's project]
comments: true
mathjax: true
author: Seokjun Kim
---

{: .box-note}
**Assignment 1**

Using SAT solver(Z3 solver), solve puzzles.

**1) Sudoku**
<br>
Sudoku is a popular logic-based puzzle game that involves filling a 9x9 grid with digits so that each column, each row, and each of the nine 3x3 subgrids (called "regions") contains all of the digits from 1 to 9 without repetition. The puzzle starts with some cells already filled in, and the goal is to fill in the empty cells while following the rules.

![sudoku](https://withalliam.github.io/assets/img/sudoku.png)

[sudoku.c](https://github.com/withalliam/Bachelors/blob/main/Discrete_mathematics/PA1/sudoku.c)

**2) Anti-king Sudoku**
<br>
Anti-King Sudoku is a variant of the traditional Sudoku puzzle that adds an extra layer of challenge by introducing a new constraint related to the placement of the digit 9. In Anti-King Sudoku, the digit 9 cannot appear orthogonally adjacent to another 9, similar to the movement of a chess king.

[antiking_sudoku.c](https://github.com/withalliam/Bachelors/blob/main/Discrete_mathematics/PA1/antiking_sudoku.c)

**3) Nondango**
<br>
Nondango is a puzzle divided into 13 to 50 regions at a given 10*10 board. Each region contains at least two a maximum of eight connected cells, and some cells contain a circle. Also, initially all of these circles are white, and we have to follow the rules below and color them. Exactly one black circle must exist in each region and no circles of the same color must be placed in three successive cells. (Region is irrelevant) This puzzle can eventually be considered a matter of finding where the black circles should be located for a given problem. In other words, when imagining that a black circle is located in a cell, if a situation inevitably violates the conditions, (contradiction) the cell can be seen as a cell containing a white circle.

![nondango](https://withalliam.github.io/assets/img/nondango.png)

[nondango.c](https://github.com/withalliam/Bachelors/blob/main/Discrete_mathematics/PA1/nondango.c)

**4) Gappy**
<br>
The Gappy puzzle is a 9x9 grid-based logic game where each cell can be filled with either black or white. The puzzle's main rule is that no two black cells may touch, not even diagonally, ensuring there is at least one white cell separating them. Additionally, each row and each column must contain exactly two black cells. Numbers provided on each row and column indicate the count of white cells between the two black cells. The possible range for these labels is from zero to seven due to the grid's dimensions. To solve a Gappy puzzle, one would typically use a SAT (Boolean satisfiability problem) solver that determines if a set of conditions can be met.

[gappy.c](https://github.com/withalliam/Bachelors/blob/main/Discrete_mathematics/PA1/gappy.c)

**5) N-queen problem**
<br>
The N-Queen problem is a classic puzzle that challenges players to place N queens on an NxN chessboard without any queen threatening another. The objective is to find all possible arrangements of queens on the board that satisfy this condition. Queens can move horizontally, vertically, or diagonally without obstruction. The challenge arises from the necessity to ensure no two queens share the same row, column, or diagonal. The N-Queen problem is a well-known example of a constraint satisfaction problem in computer science and mathematics. Solutions often involve recursive backtracking algorithms or other efficient techniques to explore and eliminate invalid arrangements until a valid solution is found.

![n-queen](https://withalliam.github.io/assets/img/n-queen.png)

[nqueen-sat.c](https://github.com/withalliam/Bachelors/blob/main/Discrete_mathematics/PA1/nqueen-sat.c)

{: .box-note}
**Assignment 2**


{: .box-note}
**Assignment 3**