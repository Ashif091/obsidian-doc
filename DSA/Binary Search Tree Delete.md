![[Pasted image 20240306134456.png||500]]
![[Pasted image 20240306134929.png||500]]
![[Pasted image 20240306135108.png||500]]
```javascript
delete(value) {
	this.root = this.deleteNode(this.root, value);
}

deleteNode(root, value) {
	if(root === null) {
		return root;
	}
	
	if (value < root.value) {
		root.left = this.deleteNode(root.left, value);
	} else if (value > root.value) {
		root.right = this.deleteNode(root.right, value);
	} else {
			if(!root.left && !root.right) {
				return null;
			}
			if(!root.left) {
				return root.right;
			} else if(!root.right) {
				return root.left;
			}

			root.value = this.min(root.right);
			root.right = this.deleteNode(root.right, root.value);
		}
	return root;
}
```