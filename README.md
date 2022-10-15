# dijkstras-algorithm

[Please follow the visual guide first.](https://github.com/anthonymcglone2022/dijkstras-algorithm/blob/master/Dijkstra's%20algorithm.pdf)

When done, follow the comments in the pseudocode below.

```java
 1  function dijkstra_algorithm(graph, source): // Pass in the graph (with vertices and edges) and choose the source node.
 2      
 3      for each vertex v in graph.vertices: // For each node, set the temporary distance to infinity.
 4          dist[v] ← INFINITY
 5          prev[v] ← UNDEFINED
 6          add v to Q // Add each node to the unvisited set Q.
 7      dist[source] ← 0 // Set the source node's temporary distance to 0.
 8      
 9      while Q is not empty: // Continue the algorithm while there are unvisited nodes.
10          u ← vertex in Q with min dist[u] // Set the current node to the one with the minimum temporary distance in Q.
11          remove u from Q // Mark the current node as visited.
12          
13          for each neighbour v of u still in Q: // Examine the nodes directly attached to the current node.
14              alt ← dist[u] + graph.edges(u, v) // Calculate the new temporary distance.
15              if alt < dist[v]: // Compare the temporary distance on the neighbour with the calculated temporary distance.
16                  dist[v] ← alt // If the calculated temporary distance is lower, update the neighbour.
17                  prev[v] ← u
18
19      return dist[], prev[] // Return the dist array, which has the shortest paths.
```
