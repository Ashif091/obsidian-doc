```js
class Node {
   constructor (value){
      this.value = value
      this.next = null
   }
}

  

class LinkedList {
   constructor() {
      this.head = null
      this.size = 0
   }
   isEmpty(){
      return this.size ===0
   }
   getSize(){
      return this.size
   }
}

let list = new LinkedList()

console.log("List is emty ?", list.isEmpty()) //List is emty ? true
console.log("List size", list.getSize())//List size 0
```



