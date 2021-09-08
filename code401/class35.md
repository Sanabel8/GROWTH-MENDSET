# Graphs
* A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.
* common terminology used when working with Graphs:
1. Vertex 
2. Edge : An edge is a connection between two nodes.
3. Neighbor  : The neighbors of a node are its adjacent nodes
4. Degree :  The degree of a vertex is the number of edges connected to that vertex.
# Directed vs Undirected
1. Undirected Graphs :  is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.

# Directed Graphs (Digraph)
* A Directed Graph also called a Digraph is a graph where every edge is directed.

# Complete vs Connected vs Disconnected
* The three different types are completed, connected, and disconnected.
* This depends on how connected the graphs are to other node/vertices.

### Complete Graphs : A complete graph is when all nodes are connected to all other nodes.
### Connected : A connected graph is graph that has all of vertices/nodes have at least one edge.
### Disconnected : A disconnected graph is a graph where some vertices may not have edges.

# Acyclic vs Cyclic
### Acyclic Graph : An acyclic graph is a directed graph without cycles , is also called a DAG.
### Cyclic Graphs : A Cyclic graph is a graph that has cycles,  as a path of a positive length that starts and ends at the same vertex.

# Graph Representation
We represent graphs through:
1. Adjacency Matrix
2. Adjacency List
* Adjacency Matrix : is represented through a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matrix
* Each Row and column represents each vertex of the data structure. The elements of both the column and the row must add up to 1 if there is an edge that connects the two, or zero if there isn’t a connection.
* Adjacency List : An adjacency list is the most common way to represent graphs.

### Weighted Graphs
* A weighted graph is a graph with numbers assigned to its edges. These numbers are called weights. This is what a weighted graph looks like:

#traversals
### Breadth First
*  Breadth first traversal is when you visit all the nodes that are closest to the root as possible. From there you traverse outwards, level by level, until you have visited all the vertices/nodes.
* Here is what the algorithm breadth first traversal looks like:
1. Enqueue the declared start node into the Queue.
2. Create a loop that will run while the node still has nodes present.
3. Dequeue the first node from the queue
4. if the Dequeue‘d node has unvisited child nodes, add the unvisited children to visited set and insert them into the queue.
* This is the code for a breadth first traversal:

```ALGORITHM BreadthFirst(vertex)
    DECLARE nodes <-- new List()
    DECLARE breadth <-- new Queue()
    DECLARE visited <-- new Set()

    breadth.Enqueue(vertex)
    visited.Add(vertex)

    while (breadth is not empty)
        DECLARE front <-- breadth.Dequeue()
        nodes.Add(front)

        for each child in front.Children
            if(child is not visited)
                visited.Add(child)
                breadth.Enqueue(child)   

    return nodes;
```

### Depth First
* The algorithm for a depth first traversal is as follows:
1. Push the root node into the stack
2. Start a while loop while the stack is not empty
3. Peek at the top node in the stack
4. If the top node has unvisited children, mark the top node as visited, and then Push any unvisited children back into the stack.
5. If the top node does not have any unvisited children, Pop that node off the stack
6. repeat until the stack is empty.
































