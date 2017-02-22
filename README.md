# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: In sudoku, a "naked twin" refers to a set of two candidate digits located in two boxes that share at least one unit.  If, for example, we have {'A5': '13', 'A6': '13',...} then we can deduce that 1 and 3 must be in A5 and A6.  Even though we do not yet know which digit belongs to which box, we can still eliminate the same digits from all the other peer boxes.  In order to perform constraint propagation to solve this problem, boxes that are peers to each other and have the same 2 possible digits will first need to be identified.  Then, the two numbers will need to be eliminated from all other boxes that are peers to the two previously identified boxes.  Therefore, this strategy reduces the number of possibilities for the two boxes' peers, and the peers of those peers, and so on - hence constraint propagation.  The code becomes even more efficient in solving sudoku puzzles when the naked twins strategy is coupled to other strategies such as elminiate and only choice.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: *Student should provide answer here*

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.
