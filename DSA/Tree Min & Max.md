
![[Pasted image 20240306134054.png]]
```js
    max(Root){
        if(!Root.right){
            return Root.value
        }else{
            return this.max(Root.right)
        }
    }
```

![[Pasted image 20240306134106.png]]

```js
    min(Root){
        if(!Root.left){
            return Root.value
        }else{
           return this.min(Root.left)
        }
    }

```

