# dijkstras-algorithm

Please read the PDF first. When done, follow the comments in the pseudocode below.

```java
 1  function dijkstra_algorithm(graph, source): // Pass in the 'graph' (with vertices and edges) and choose the 'source' node
 2      
 3      for each vertex v in graph.vertices:
 4          dist[v] ← INFINITY
 5          prev[v] ← UNDEFINED
 6          add v to Q
 7      dist[source] ← 0
 8      
 9      while Q is not empty:
10          u ← vertex in Q with min dist[u]
11          remove u from Q
12          
13          for each neighbor v of u still in Q:
14              alt ← dist[u] + graph.edges(u, v)
15              if alt < dist[v]:
16                  dist[v] ← alt
17                  prev[v] ← u
18
19      return dist[], prev[]
```
