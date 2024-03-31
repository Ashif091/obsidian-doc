1. Visit the left subtree
2.  Visit the right subtree
3. Read the data of the node

![[Pasted image 20240306115915.png||500]]

```js
    postOrder(Root){
        if(Root){
            this.preOrder(Root.left)
            this.preOrder(Root.right)
            console.log(Root.value);
        }
    }
```