![[Pasted image 20240207200255.png]]

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

   print(){
      if(this.isEmpty()){
         console.log(`the list is emty ?`);
      }else{
         let listValues = ''
         let curr = this.head
         while(curr){
            listValues +=`${curr.value} `
            curr = curr.next
         }
         console.log(listValues);

      }

   }

}

  

let list = new LinkedList()
console.log("List is emty ?", list.isEmpty())
console.log("List size", list.getSize()) 
list.prepend(10)
list.prepend(20)
list.prepend(40) 
list.print()
```