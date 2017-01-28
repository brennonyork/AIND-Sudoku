# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A:

> We use constraint propagation to solve the naked twins problem by identifying
> multiple cells within a given unit that only contain two possible values. If
> two separate cells contain the same two numbers then it can be reasoned that
> only those two numbers can exist in those two cells, agnostic of what those
> cells' individual values are. The identification of these two values in these
> two cells *constrains* the larger sudoku problem and allows the solver to
> *propagate* these constraints so as to minimize the problem landscape (eg
> the sudoku board).

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A:

> The diagonal sudoku problem is a further constraint on the generalized sudoku
> problem in such that both diagonals must also only contain only the values one
> through nine. We use constraint propagation to solve this by further extending
> the core methods ('elimination' and 'only choice') to incorporate the diagonals.
> Ensuring the rule of diagonals also suffices adds new units to the `unitlist`
> and thus new *constraints* that one can *propagate* to further minimize the
> overall set of choices the 'elimination' and 'only choice' methods have available
> when solving the larger sudoku problem.

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
