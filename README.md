# CI2024_lab2
# n^2 -1 Puzzle Problem

This repository contains the solution to the n puzzle problem implemented in the Jupyter Notebook `n-puzzle.ipynb` by the student Luca Ianniello, s327313.

## Algorithm Explanation

### A* Search Algorithm
The A* algorithm is a pathfinding algorithm that uses both the path cost (number of moves) and a heuristic (Manhattan distance) to guide the search toward the goal state efficiently.

#### Initialization:
- The initial puzzle state is added to the open list with a cost based on its Manhattan distance.

#### Exploring Nodes:
- The algorithm selects the state with the lowest total estimated cost (moves made + Manhattan distance).
- It then generates possible moves (neighbors) from the current state by sliding tiles into the empty space.

#### Heuristic - Manhattan Distance:
- The heuristic is calculated by summing the horizontal and vertical distances of each tile from its goal position.
- This helps prioritize states that are closer to the solved configuration, reducing the number of nodes expanded.

#### Goal Test:
- When the algorithm finds the goal state, it returns the solution path (sequence of moves), the quality of the solution (number of moves), and the cost (total nodes evaluated).

### Why Use Manhattan Distance?
Manhattan distance is **admissible**, meaning it never overestimates the number of moves to the goal. This ensures that A* will find the shortest solution path. It provides a good balance of **computational efficiency** and **accuracy**.

## Features

- **Efficient Solving of Custom Puzzle Sizes**: Easily change the puzzle dimension (e.g., 3x3, 4x4, 5x5).
- **Quality and Cost Tracking**: Outputs the number of moves and the total nodes evaluated, allowing analysis of solution efficiency.
- **Random Initial State**: The puzzle can be randomized using `RANDOMIZE_STEPS`, a parameter controlling the number of random moves applied from the solved state.
