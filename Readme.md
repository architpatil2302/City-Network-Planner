# Minimum-Cost City Network Planner Using Kruskal's Algorithm

## 1. Project Overview

The Minimum-Cost City Network Planner is a menu-driven application developed in the C programming language. It uses Kruskal's Algorithm to find the Minimum Spanning Tree (MST) of a weighted, undirected graph.

The project helps connect multiple cities with the minimum total connection cost while avoiding cycles.

## 2. Objectives

- Understand and implement Kruskal's Greedy Algorithm.
- Represent cities as vertices and connections as weighted edges.
- Find the Minimum Spanning Tree.
- Minimize the total cost of connecting all cities.
- Detect and display cycle-forming edges.
- Identify disconnected networks where an MST cannot be formed.

## 3. Technologies Used

- **Programming Language:** C
- **Concepts:** Graphs, Greedy Algorithm, Minimum Spanning Tree
- **Data Structures:** Structures, Arrays, Disjoint Set Union
- **Cycle Detection:** Parent and Rank arrays
- **Compiler:** GCC or any standard C compiler

## 4. Features

- Enter city names.
- Add multiple connections in one operation.
- Specify the source city, destination city, and connection cost.
- Display all cities and connections.
- Sort connections by increasing cost.
- Generate the Minimum Spanning Tree using Kruskal's Algorithm.
- Display selected and rejected edges.
- Calculate the total minimum cost.
- Detect disconnected networks.
- Use a menu-driven interface.

## 5. Algorithm

1. Accept the number and names of cities.
2. Accept all connections and their costs.
3. Sort all edges in ascending order of cost.
4. Initialize the parent and rank arrays.
5. Process the edges in sorted order.
6. Find the roots of the source and destination vertices.
7. If their roots differ, accept the edge and combine the sets.
8. If their roots are the same, reject the edge because it creates a cycle.
9. Continue processing the edges.
10. If exactly `V - 1` edges are selected, display the MST and total cost.
11. Otherwise, report that the network is disconnected.

## 6. How to Run the Project

### Step 1: Save the source code

Save the C program as `main.c`.

### Step 2: Compile the program

Using GCC, run:

```bash
gcc main.c -o city_network
```

### Step 3: Execute the program

On Linux or macOS:

```bash
./city_network
```

On Windows:

```bash
city_network.exe
```

## 7. Sample Input

### Enter Cities

```text
5
A
B
C
D
E
```

### Enter Connections

Select menu option 2 and enter:

```text
6
A B 10
A C 5
B C 3
B D 8
C D 6
D E 4
```

Each connection consists of:

```text
Source Destination Cost
```

## 8. Sample Output

After entering all connections, select menu option 5.

```text
KRUSKAL'S ALGORITHM

Connection    Cost    Decision
B - C         3       ACCEPT
D - E         4       ACCEPT
A - C         5       ACCEPT
C - D         6       ACCEPT
B - D         8       REJECT - CYCLE
A - B         10      REJECT - CYCLE

Minimum Spanning Tree created successfully.
Total Minimum Cost = 18
```

### Minimum Spanning Tree

```text
B - C : 3
D - E : 4
A - C : 5
C - D : 6

Total Minimum Cost = 18
```

## 9. Complexity Analysis

Let `V` be the number of vertices and `E` be the number of edges.

- **Sorting:** `O(E log E)` using an efficient sorting algorithm; the current implementation uses bubble sort, which takes `O(E²)`.
- **Cycle Detection:** Uses Disjoint Set Union with path compression and union by rank.
- **Overall Time Complexity:** `O(E²)` for the current bubble-sort implementation, plus near-linear disjoint-set processing.
- **Space Complexity:** `O(V + E)` for storing the graph, MST, rejected edges, and disjoint-set arrays.

## 10. Applications

- Planning road networks between cities.
- Designing computer and communication networks.
- Connecting electrical power distribution points.
- Planning cable and pipeline networks.
- Minimizing the cost of connecting multiple locations.

## 11. Limitations

- The program supports a maximum of 50 cities.
- The program supports a maximum of 100 connections.
- Connection costs must be non-negative.
- An MST can only be formed when all cities are connected through the available edges.

## 12. Conclusion

The project demonstrates the practical application of Kruskal's Greedy Algorithm for finding a Minimum Spanning Tree. It selects minimum-cost connections while avoiding cycles and calculates the minimum total cost required to connect all cities.

The project provides practical experience with graph algorithms, sorting, data structures, and Disjoint Set Union in C.
