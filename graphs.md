# Graphs

Non-linear data structure that can be looked at as a collection of `vertices` (or `nodes`) potentially connected by line segments names `edges`.

**All data structures we've been exposed to up to this point could be represented as graphs**

- Graphs exist in order to hold connections to things, they also exist when the connections hold information also

- **Undirected Graph:** graph where each edge is undirected or bi-directional. Means that it doesn't move in any direction.

- **Directed Graph (Digraph):** graph where every edge is directed. Has direction.

- **Complete:** each vertice (node) is connected to every other vertice

- **Connected:** all nodes have at lease one edge (a tree is a form of connected graph)

- **Disconnected:** some vertices may not have edges (can have standalone nodes or edges- aka islands)

- Cycle is when a node can be traversed through and potentially end up back at itself. Path of positive length that starts and ends at the same vertex.

- **Acyclic:** directed graph without cycles

   - **DAG:** directed acyclic graph, we know them as trees
- **Cyclic:** graph that has cycles

- **Graph Representation**

   - **Adjancency Matrix**
      - 2D array
      - n nodes is n x n boolean matrix
   - **Adjancency List**
      - collection of linked lists or array that lists all other vertices connected
      - more common than adjancency matrix
- **Weighted Graph:** graph with numbers (weights) assigned to its edges

   - Best to use hashtable structure as you'll need to store key/value pairs
- **Traversals** (like trees!)

   - **Breadth first**
```    ALGORITHM BreadthFirst(vertex)
    DECLARE nodes <-- new List()
    DECLARE breadth <-- new Queue()
    breadth.Enqueue(vertex)

    while (breadth is not empty)
        DECLARE front <-- breadth.Dequeue()
        nodes.Add(front)

        for each child in front.Children
            if(child is not visited)
                child.Visited <-- true
                breadth.Enqueue(child)   

    return nodes;
```
- **Depth first**
   - Push the root node into the stack
   - Start a while loop while the stack is not empty
   - Peek at the top node in the stack
   - If the top node has unvisited children, mark the top node as visited, and then Push any unvisited children back into the stack.
   - If the top node does not have any unvisited children, Pop that node off the stack
   - repeat until the stack is empty.
   
- **Graphs in the Real World**
   - GPS and Mapping
   - Driving Directions
   - Social Networks
   - Airline Traffic
   - Netflix uses graphs for suggestions of products


| **Term** |	**Definition** |
|------|---------------|
| ***Vertex / Node*** |	A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.|
| ***Edge*** |	An edge is a connection between two nodes.|
| ***Neighbor*** |	The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.|
| ***Degree*** |	The degree of a vertex is the number of edges connected to that vertex.|