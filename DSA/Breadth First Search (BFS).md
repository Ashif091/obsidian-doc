Explore all nodes at the present depth prior to moving on to the nodes at the next depth level

![[Pasted image 20240306122932.png||500]]
﻿

### BFS Traversal Approach
1. Create a queue
2. Enqueue the root node
3. As long as a node exists in the queue
	a. Dequeue the node from the front
	b. Read the node's value
	C. Enqueue the node's left child if it exists
	d. Enqueue the node's right child if it exists


![[Pasted image 20240306130440.png]]


```js
    BFT(root){
        let queue = []
        if(root){
            queue.push(root)
            while(queue.length){
                let curr = queue.shift()
                console.log(curr.value);
                if(curr.left){
                    queue.push(curr.left)
                }
                if(curr.right){
                    queue.push(curr.right)
                }
            }
        }
    }
```

