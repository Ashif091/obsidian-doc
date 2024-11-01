

- A graph is a non-linear data structure that consists of a finite number of vertices (also called nodes) connected by edges
- Trees are a specific type of graph data structure

### Types of Graph 
#### Directed Graph
![[Pasted image 20240308110242.png||600]]
#### Undirected Graph
![[Pasted image 20240308110248.png||600]]

#### More graph types

![[Pasted image 20240308110854.png||600]]







### Graph Representation
 [[Adjacency Matrix of a Graph]]
 [[Adjacency List of a Graph]]

### Adjacency Matrix 🆚 Adjacency List
|                                                                  |                                                                            |
| ---------------------------------------------------------------- | -------------------------------------------------------------------------- |
| Matrix                                                           | List                                                                       |
| Store the values irrespective of whether and edge exists or not. | Only need to store the va**l**ues for the edges that exist.                |
| Not efficient storage vise                                       | More efficient storage wise                                                |
| Insertion and search is O(n)                                     | Inserting and finding is O(1)                                              |
| Additional information would have to be stored externally.       | Allows to store additional values with and edge such as weight of the edge |
```js
class Graph {
  constructor() {
    this.adjacencyList = {};
  }

  addVertex(vertex) {
    if (!this.adjacencyList[vertex]) {
      this.adjacencyList[vertex] = new Set();
    }
  }

  addEdge(vertex1, vertex2) {
    if (!this.adjacencyList[vertex1]) {
      this.addVertex(vertex1);
    }
    if (!this.adjacencyList[vertex2]) {
      this.addVertex(vertex2);
    }
    this.adjacencyList[vertex1].add(vertex2);
    this.adjacencyList[vertex2].add(vertex1);
  }

  removeEdge(vertex1, vertex2) {
    this.adjacencyList[vertex1].delete(vertex2);
    this.adjacencyList[vertex2].delete(vertex1);
  }

  removeVertex(vertex) {
    if (!this.adjacencyList[vertex]) {
      return;
    }
    for (let adjacentVertex of this.adjacencyList[vertex]) {
      this.removeEdge(vertex, adjacentVertex);
    }
    delete this.adjacencyList[vertex];
  }

  hasEdge(vertex1, vertex2) {
    return (
      this.adjacencyList[vertex1].has(vertex2) &&
      this.adjacencyList[vertex2].has(vertex1)
    );
  }

  display() {
    for (let vertex in this.adjacencyList) {
      console.log(vertex + " -> " + [...this.adjacencyList[vertex]]);
    }
  }
}

const graph = new Graph();
graph.addVertex("A");
graph.addVertex("B");
graph.addVertex("C");
graph.addEdge("A", "B");
graph.addEdge("A", "C");
graph.addEdge("B", "C");
graph.display();
graph.removeEdge("A", "B");
graph.display();
graph.removeVertex("A");
graph.display();

```


## BFS and DFS

```js
function bfs(graph, startNode) {
  let queue = [startNode];
  let visited = new Set();

  while (queue.length > 0) {
    let currentNode = queue.shift();

    if (!visited.has(currentNode)) {
      console.log(currentNode);
      visited.add(currentNode);

      graph[currentNode].forEach(neighbor => {
        if (!visited.has(neighbor)) {
          queue.push(neighbor);
        }
      });
    }
  }
}

function dfs(graph, startNode, visited = new Set()) {
  if (visited.has(startNode)) return;

  console.log(startNode);
  visited.add(startNode);

  graph[startNode].forEach(neighbor => {
    dfs(graph, neighbor, visited);
  });
}
```


## Cycle Detection in Undirected Graphs

```js
function isCyclicUndirected(graph) {
  const visited = new Set();

  function dfs(v, parent) {
    visited.add(v);

    for (const neighbor of graph[v]) {
      if (!visited.has(neighbor)) {
        if (dfs(neighbor, v)) return true;
      } else if (neighbor !== parent) {
        return true;
      }
    }

    return false;
  }

  for (const vertex in graph) {
    if (!visited.has(vertex)) {
      if (dfs(vertex, null)) return true;
    }
  }

  return false;
}

const graphUndirected = {
  0: [1, 2],
  1: [0, 2],
  2: [0, 1, 3],
  3: [2]
};

console.log(isCyclicUndirected(graphUndirected)); // Output: true

```