```js
  isBST(root) {
   if(!root)return true
   if(root.right && root.right.value <=root.value)return false
   if(root.left && root.left.value >=root.value)return false
   return this.isBST(this.left)&&this.isBST(this.right)
  }
```