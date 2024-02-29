![[Pasted image 20240207171140.png||600]]


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

   prepend(value){

      const node = new Node(value)

      if(this.isEmpty()){

         this.head = node

      }else{

         node.next =  this.head

         this.head = node

      }

      this.size++

   }

}

  

let list = new LinkedList()

  

console.log("List is emty ?", list.isEmpty())

console.log("List size", list.getSize())

  

list.prepend(10)

list.prepend(20)

list.prepend(40)
```