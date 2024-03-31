
![[Pasted image 20240303132450.png||500]]


```javascript
class Node {
    constructor(value) {
        this.value = value;
        this.left = null;
        this.right = null;
    }
}

class BinarySearchTree {
    constructor() {
        this.Root = null;
    }
    isEmpty() {
        return this.Root === null;
    }
    insert(value) {
        let newNode = new Node(value);
        if (this.isEmpty()) {
            this.Root = newNode;
        } else {
            this.insertNode(this.Root, newNode);
        }
    }
    insertNode(Root, newNode) {
        if (newNode.value < Root.value) {
            if (Root.left === null) {
                Root.left = newNode;
            } else {
                this.insertNode(Root.left, newNode);
            }
        } else {
            if (Root.right === null) {
                Root.right = newNode;
            } else {
                this.insertNode(Root.right, newNode);
            }
        }
    }
    search(root, value) {
        if (!root) {
            return false;
        }
        if (root.value === value) {
            return true;
        } else {
            if (value < root.value) {
                return this.search(root.left, value);
            } else {
                return this.search(root.right, value);
            }
        }
    }
}

let BST = new BinarySearchTree();

BST.insert(12);
BST.insert(2);
BST.insert(42);
BST.insert(5);

console.log(BST.search(BST.Root, 12));
console.log(BST.search(BST.Root, 4));
console.log(BST.search(BST.Root, 5));
console.log(BST.search(BST.Root, 42));
```

