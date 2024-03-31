![[Pasted image 20240302082317.png||400]]


```js
class Node {
    constructor(value) {
        this.value = value
        this.left = null
        this.right = null
    }
}

class BinarySearchTree {
    constructor() {
        this.Root = null
    }
    isEmpty() {
        return this.Root === null
    }
    insert(value) {
        let newNode = new Node(value)
        if (this.isEmpty()) {
            this.Root = newNode
        } else {
            this.insertNode(this.Root, newNode)
        }
    }
    insertNode(Root, newNode) {
        if (newNode.value < Root.value) {
            if (Root.left === null) {
                Root.left = newNode
            } else {
                this.insertNode(Root.left, newNode)
            }
        } else {
            if (Root.right === null) {
                Root.right = newNode
            } else {
                this.insertNode(Root.right, newNode)
            }
        }
    }
}

let bst = new BinarySearchTree();
bst.insert(10);
bst.insert(5);
bst.insert(15);
bst.insert(3);
bst.insert(7);
bst.insert(12);
bst.insert(17);

```

```js
class binarySearchTree {
    constructor() {
        this.root = null
    }
    isEmpty() {
        return this.root === null
    }
    insert(value) {
        let newNode = new Node(value)
        if (this.isEmpty()) {
            this.root = newNode
        } else {
           this.root =  this.insertNode(this.root, newNode)
        }
    }
    insertNode(root, newNode) {
        if (!root) {
            root = newNode
        } else {
            if (newNode.value < root.value) {
                root.left = this.insertNode(root.left, newNode)
            } else {
                root.right = this.insertNode(root.right, newNode)
            }
        }
        return root
    }
}
```