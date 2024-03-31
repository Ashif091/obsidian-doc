1. Visit the left subtree
2.  Read the data of the node
3. Visit the right subtree

![[Pasted image 20240306115759.png||500]]

```js
    inOrder(Root){
        if(Root){
            this.preOrder(Root.left)
            console.log(Root.value);
            this.preOrder(Root.right)
        }

    }
```