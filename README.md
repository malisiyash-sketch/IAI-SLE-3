# IAI-SLE-3
Knight's Shortest Path — BFS vs DFS

1. Project Title

Knight's Shortest Path using BFS and DFS

2. Student Information

- Name: SUYASH MALI
- PRN: 25UAM107
- Course: 02AML204 – Introduction to Artificial Intelligence
- Division: B

3. Project Description

This project finds a path for a chess knight from a starting square to a target square on a standard 8×8 chessboard.

For this experiment, the starting position is a1 and the target position is h8.

The system implements and compares two search algorithms:

- Breadth-First Search (BFS)
- Depth-First Search (DFS)

Each chessboard square is treated as a node, and each legal knight move is treated as an edge. The system finds a path and records performance information such as path length, nodes expanded, and execution time.

4. Objective

The main objectives are:

1. Find a path from a1 to h8.
2. Implement BFS and DFS for the same knight-move problem.
3. Compare the behaviour and performance of BFS and DFS.
4. Measure execution time and nodes expanded.
5. Understand why BFS is suitable for finding the shortest path.

5. Algorithms Used

Breadth-First Search (BFS)

BFS explores the search space level by level using a queue.

For this problem, BFS guarantees the shortest path because every legal knight move has the same cost.

Depth-First Search (DFS)

DFS explores one branch deeply before backtracking. It uses a stack.

DFS can find a path without guaranteeing that the path is the shortest one.

6. Input

- Board size: 8 × 8
- Starting square: a1
- Goal square: h8
- Search algorithms: BFS and DFS

7. Main Functions

knight_moves(square)

Returns the legal destinations for a given chessboard square.

bfs(start, goal)

Performs Breadth-First Search and finds the shortest path.

dfs(start, goal)

Performs Depth-First Search and returns the first path found.

reconstruct_path(parent, goal)

Reconstructs the final path using the parent/came-from information.

time_algorithm(search_fn)

Measures the execution time of a search algorithm.

run_experiment()

Runs BFS and DFS and records path length, nodes expanded, and timing.

8. Results

The experiment was performed using five runs for each algorithm.

Metric| BFS| DFS
Average Time| 0.0656 ms| 0.0573 ms
Best Time| 0.0604 ms| 0.0403 ms
Worst Time| 0.0798 ms| 0.0821 ms
Nodes Expanded| 64| 35
Path Length| 6 moves| 18 moves

BFS found the mathematically shortest path of 6 moves, while DFS found an 18-move path in the measured run.

9. Conclusion

The project demonstrates the difference between BFS and DFS for the Knight's Shortest Path problem.

BFS guarantees the shortest path because it explores nodes level by level. DFS may find a path faster in some cases, but it does not guarantee the shortest path.

The experiment also provides a basis for the SLE-3 architectural design using the complete C4 Model: Context, Container, Component, and Code.

10. SLE-3 Architecture

The system is represented using four C4 levels:

1. Context Diagram – Shows the user interacting with the Knight's Shortest Path System.
2. Container Diagram – Shows the major parts such as input/validation, search engine, visited set/frontier, path reconstruction, and output/metrics.
3. Component Diagram – Shows the internal components of the Search Engine.
4. Code Level – Shows the important functions used by the system.

11. Requirements

- Python 3.x
- Python standard libraries required by the project code
- Any IDE or code editor such as VS Code, PyCharm, or IDLE

12. How to Run

1. Open the project/code in a Python-compatible IDE.
2. Make sure Python 3.x is installed.
3. Run the main Python program.
4. The program executes the Knight's Shortest Path search using BFS and DFS.
5. Observe the resulting path and performance metrics.

13. Project Structure

Knight-Shortest-Path/
│
├── knight_shortest_path.py
├── README.md
├── AI_Contribution_Log
└── SLE-3_Report.docx

14. AI Contribution

AI assistance was used during development for BFS/DFS search code, timing and node-counting support, path-visualization ideas, and report structure.

The student reviewed and ran the experiments, checked the reported results, selected the problem, and reviewed the architecture and justification.
