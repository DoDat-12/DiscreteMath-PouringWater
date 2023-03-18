# Pouring Water
## Problem
We have three containers with volumes of $10$ liters, $7$ liters, and $4$ liters. Initially, the $7$-liter and $4$-liter containers are full of water, while the $10$-liter container is empty. We are only allowed to use the following operation: Pour all the remaining water from one container into another container, stopping only when the other container is full or the first container is empty.

Pour water problem: With a sequence of operations like this, can we leave exactly $2$ liters of water in a $4$-liter container or $2$ liters of water in a $7$-liter container?

To solve this problem, we construct a directed graph $G=(V,E)$ where:

- The set of vertices $V$ is the set of non-negative integer triples $(x,y,z)$ where $x, y$ and $z$ are the amount of water in the three jugs of $10$ liters, $7$ liters and $4$ liters, respectively. For example, the vertex $(0,7,4)$ represents: the jug of $10$ liters is empty, while the jugs of $7$ liters and $4$ liters are full of water. 
- There is an edge from vertex $(x,y,z)$ to vertex $(x’, y’, z’)$ if we can use the pouring operation as described above to get from $(x,y,z)$ to $(x’,y’,z’)$. For example, $(0, 7, 4) \to (4,7,0) \to (10, 1, 0)$ means that we pour all the water from the jug of $4$ liters into the jug of $10$ liters, and then fill the jug of $10$ liters from the jug of $7$ liters. Please run the DFS algorithm on this graph $G$ starting from the vertex $(0,7,4)$ to find the solution to the water pouring problem.

### Requirement
Please draw the DFS tree (no need for dashed edges) using Graphviz starting from the vertex $(0,7,4)$. If you need to decide the order of visited vertices, please use a natural order according to you.
