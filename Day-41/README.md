Data Structures and Algorithms (DSA), a graph is a way to represent relationships between objects. It consists of:

Vertices (or nodes): These are the objects or points.

Edges: These are the connections between the vertices.

**Graphs can be:**

Directed (DiGraph): Edges have a direction, like A → B.

Undirected: Edges don’t have a direction, like A — B.

**Other features:**

Weighted: Edges have values (e.g., distance, cost).

Unweighted: Edges just show connection, no values.

Graphs are used to model things like social networks, road maps, flight routes, and network connections.



**Graph Representation**

DSA, graph representation means how we store a graph in memory. There are two main ways:

**Adjacency Matrix**

A 2D array of size V × V (V = number of vertices)

matrix[i][j] = 1 if there is an edge between vertex i and j (or weight if weighted)

Easy to check if an edge exists, but uses more space (O(V²))

**Adjacency List**

An array of lists, where each index represents a vertex and stores all its neighbors

Space-efficient for sparse graphs (O(V + E), E = number of edges)

Iterating neighbors is faster

**Example:**

**Vertices** = {A, B, C}
**Edges** = {(A, B), (B, C)}
