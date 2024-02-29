- The queue data structure is a sequential collection of elements that follows the principle of First In First Out (FIFO)
- The first element inserted into the queue is first element to be removed
- A queue of people. People enter the queue at one end (rear/tail) and leave the queue from the other end (front/ head).
- Queue is an abstract data type. It is defined by its behavior rather than being a mathematical model
- The Queue data structure supports two main operations
	- ***Enqueue***, which adds an element to the rear/tail of the collection
	- ***Dequeue***, which removes an element from the front/head of the collection

![[Pasted image 20240215144153.png]]![[Pasted image 20240215144156.png]]


## Queue Usage
- Printers
- CPU task scheduling
- Callback queue in JavaScript runtime
- [[Circular Queue]]

﻿

## Queue Implementation
- enqueue(element) - add an element to the queue
- dequeue() - remove the oldest element from the queue
- peek()- get the value of the element at the front of the queue without removing it
- isEmpty() - check if the queue is empty
- size() - get the number of elements in the queue
- print()- visualize the elements in the queue

# Array method 
```js
class Queue{
    constructor(){
        this.items = []
    }

    enqueue(element){
        this.items.push(element)
    }

    dequeue(){
        return this.items.shift()
    }

    isEmpty(){
        return this.items.length === 0
    }
    peek(){
        if(!this.isEmpty()){
            return this.items[0]
        }
        return null
    }
    print(){
        console.log(this.items.toString())
    }
}
```



# Object method 
```js
class Queue{
    constructor (){
        this.items = {}
        this.rear = 0
        this.front = 0
    }
    enqueue(element){
        this.items[this.rear] = element
        this.rear++
    }
    dequeue(){
        let items = delete this.items[this.front]
        this.front++
        return items
    }

    isEmpty(){
        return this.rear - this.front === 0
    }
    peek(){
        if(!this.isEmpty()){
            return this.items[this.front]
        }
        return null
    }
    print(){
        console.log(this.items)
    }
}
```


```js
class Node {
  constructor(value) {
    this.value = value;
    this.next = null;
  }
}

class Queue {
	  constructor() {
	    this.head = null;
	  }
	
	  isEmpty() {
	    return this.head === null;
	  }
	
	  enqueue(value) {
	    let node = new Node(value);
	    if (this.isEmpty()) {
	      this.head = node;
	    } else {
	      let curr = this.head;
	      while (curr.next) {
	        curr = curr.next;
	      }
	      curr.next = node;
	    }
	  }
	
	  dequeue() {
	    let deleteNode = this.head;
	    this.head = deleteNode.next;
	    return deleteNode;
	  }
	
	  print() {
	    let curr = this.head;
	    while (curr) {
	      console.log(curr.value);
	      curr = curr.next;
	    }
	  }
}

```