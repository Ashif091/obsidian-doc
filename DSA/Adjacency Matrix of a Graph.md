- An adjacency matrix is a 2D array of size [V x V] where V is the number of vertices in the graph.
- Each row and column represent a vertex.
- If the value of any element say, matrix[i][j] is 1, it represents that there is an edge connecting vertex i and vertex j


 ```javascript
const matrix = [
// A  B  C
	[0, 1, 0], // A
	[1, 0, 1], // B
	[0, 1, 0], // C
];

// 0 means no egdes between the vertex
// 1 means there is and edge b/w those vertex

console.log(matrix[0][1]);
```

