

Stack Data Structure is a sequential collection of elements that follow the principle of Last In First Out (LIFO). That means the last element inserted will be the first to remove from the stack.

Stack is a abstract Data type. It is defined by the behavior rather than being a mathematical model.

Main operations:

- Push - Inserts data to the stack
- Pop - Remove the last element which is inserted.

### Stack Pointer

Is a memory location that points to the top element of a stack data structure in computer memory.
![[Pasted image 20240215230943.png]]
### Uses

- Browser History Tracking
- Undo Operation
- Expression Conversion
- Call stack in JS Runtime.

### Drawbacks

- Limited Access - We can access only top data. If any data other than top is required we have to repeatedly pop the top element.
- Fixed Size - In most programming language stack is implemented with fixed size, which will lead to stack overflow.
- Lack of Flexibility - Stack have limited operations. Push, pop, check if empty or is overflown are the operations, other than this it is not straight forward to do so.
- Limited Use Cases
- Resource Management
- Not suitable for all data
- Recursion Limit
- Limited Sorting



### Stack using Array
```javascript
class Stack{
	constroctor() {
		this.items = [];
	}
	
	push(value) {
		this.items.push(value);
	}
	
	pop() {
		return this.items.pop();
	}
	
	isEmpty() {
		return this.length === 0;
	}
	
	// Doesn't pop the data instead just returns; 
	peek() {
		return this.items[items.length - 1];
	}

	size() {
		return this.items.length;
	}

	print() {
		if(this.isEmpty()){
			console.log("Stack is Empty");
		} else {
			console.log(this.items.toString());
		}
	} 	
}

```

### Stack using Object

```js
class Stack {
  constructor() {
    this.items = {};
    this.head = 0;
  }

  push(element) {
    this.items[this.head] = element;
    this.head++;
  }

  pop() {
    const item = this.items[this.head - 1];
    delete this.items[this.head - 1];
    this.head--;
    return item;
  }

  peek() {
    return this.items[this.head - 1];
  }

  size() {
    return this.head;
  }

  isEmpty() {
    return this.head === 0;
  }

  print() {
    console.log(this.items);
  }
}
```


### Stack using LinkedList

Copy

```javascript
class Node {
  constructor(value) {
    this.value = value;
    this.next = null;
  }
}

class Stack {
  constructor() {
    this.head = null;
  }

  isEmpty() {
    return this.head === null;
  }

  push(value) {
    let node = new Node(value);
    if (this.isEmpty()) {
      this.head = node;
    } else {
      node.next = this.head;
      this.head = node;
    }
  }

  pop() {
    let deleteNode = this.head;
    this.head = deleteNode.next;
    return deleteNode;
  }

  display() {
    let curr = this.head;
    while (curr) {
      console.log(curr.value);
      curr = curr.next;
    }
  }

  peek() {
    if (this.isEmpty()) {
      console.log("Stack is empty");
    } else {
      return this.head.value;
    }
  }
}

```


## middle element delete
```js
class Stack {

    constructor(){

        this.items = {}

        this.head = 0

    }

  

    push(value){

        this.items[this.head] = value

        this.head++

        return true

    }

    pop(){

        let deleteData = this.items[this.head - 1]

        delete this.items[this.head - 1]

        this.head--;

        return deleteData

    }

    isEmpty(){

        return this.head === 0

    }

    size(){

        return this.head

    }

    print(){

        console.log(this.items)

    }

}

  
  

let stack = new Stack()

  

stack.push(1)

stack.push(2)

stack.push(3)

stack.push(4)

stack.push(5)

stack.print()

function middleDelete(stack){
    let store = new Stack()
    let middleIndex = Math.floor(stack.size()/2)
    for (let i = 0; i < middleIndex; i++) {
      store.push(stack.pop())          
    }
    stack.pop()
    while(!store.isEmpty()){
        stack.push(store.pop())
    }
    return true
    
}

middleDelete(stack)

  

stack.print()
```




## queue using stack

```js
class Queue{
    constructor(){
        this.stack1= []
        this.stack2= []
    }
    enqueue(value){
        this.stack1.push(value)
    }
    dequeue(){
        if(this.stack1.length + this.stack2.length === 0)return null
        if(this.stack2.length === 0){
            while (this.stack1.length !== 0) {
                this.stack2.push(this.stack1.pop()
            }
        }
        return this.stack2.pop()
    }
    print(){
     console.log([...this.stack2.reverse(),...this.stack1].toString());
    }


}
```



