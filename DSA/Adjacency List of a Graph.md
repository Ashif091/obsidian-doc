Vertices are stored in a map like DS, and every vertex stores a list of its adjacent vertices.

![[Pasted image 20240308115041.png||500]]


```javascript
let adjecencyList = {
	'A': ['B'],
	'B': ['A', 'C'],
	'C': ['B']
};

console.log(adjecencyList['B']); // prints the edges of B
```