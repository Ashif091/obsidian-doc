1. Read the data of the node
2. Visit the left subtree
3. Visit the right subtree

![[Pasted image 20240306105435.png||500]]

```js
    preOrder(Root){
        if(Root){
            console.log(Root.value);
            this.preOrder(Root.left)
            this.preOrder(Root.right)
        }
    }
```