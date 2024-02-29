![[Pasted image 20240207215714.png]]

![[Pasted image 20240207215812.png]]

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

   append(value){
      let node = new Node(value)
      if(this.isEmpty()){
         this.head = node
      }else{
         let prev = this.head
         while(prev.next){
            prev = prev.next
         }
         prev.next = node
      }
      this.size++
   }
}

  

let list = new LinkedList()
console.log("List is emty ?", list.isEmpty())
console.log("List size", list.getSize()) 
list.append(10)
list.append(20)
list.append(40) 
list.print() // 10 20 40 
```