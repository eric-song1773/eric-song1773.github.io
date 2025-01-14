---
layout: project
type: project
image: images/sudoku-image1.png
title: Recursive Sudoku Solver
permalink: projects/sudoku
# All dates must be YYYY-MM-DD format!
date: 2021-03-27
labels:
  - Java
  - Programming
  - Puzzle
summary: A sudoku solver using recursion method.
---

<img class="ui medium right floated rounded image" src="../images/sudoku-image.PNG">

For one of the projects in ICS 211, I was able to create a sudoku solver using recursion and divide-and-conquer methods. The program will take partially filled 
sudokus and brute force the set of possible numbers that can be filled out, in order to complete the sudoku. Java Eclipse IDE was used for this project. 

This project was done with the help from Professor Cam Moore and collaboration from my classmates, Jonathan M., Londy T., Christine N., and Jake H. Everyone worked together on one function at a time and helped each other out.

This project allowed me to realize the importance of collaboration, as the project was a lot more efficient with separating the job and helping each other out and learning from the help at the same time. While being able to finish the project faster due to the more students working on the project, the fact that I was able to learn from people who are the same level of me in terms of programming skills was fascinating to me.

Here is one of the major codes used to create a recursive sudoku solver. The main function of this part of the program is to find the set of possible numbers that can be used to fill out the empty cell in a 9x9 sudoku puzzle.

```Java 
/**
   * Find an assignment of values to sudoku cells that makes the sudoku valid.
   *
   * @param sudoku the sudoku to be solved
   * @return whether a solution was found if a solution was found, the sudoku is filled in with the solution if no
   * solution was found, restores the sudoku to its original value
   */
  public static boolean solveSudoku(int[][] sudoku) {
    // the sudoku is not solved yet
    boolean solved = false;
    // for each cell in the sudoku
    for (int row = 0; row < sudoku.length; row++) {
      for (int column = 0; column < sudoku.length; column++) {
        // if the cell is empty
        if (sudoku[row][column] == 0) {
          // create an ArrayList of solution with values obtained from legalValues()
          ArrayList<Integer> solution = legalValues(sudoku, row, column);
          for (int i = 0; i < solution.size(); i++) {
            // set the cell to the one of the values in solution.size()
            sudoku[row][column] = solution.get(i);
            // if the solveSudoku(sudoku) returns true, the sudoku is solved
            if (solveSudoku(sudoku)) {
              return true;
            }
          }
          // if solveSudoku(sudoku) never returns true, set the cell back to 0.
          sudoku[row][column] = 0;
          // return false
          return false;
        }
      }
    }
    // return checkSudoku(sudoku, true)
    return checkSudoku(sudoku, true);
  }
 ```
