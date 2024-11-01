```js
class Node {
    constructor(value) {
        this.value = value;
        this.next = null;
        this.prev = null;
    }
}

```

```js
class DoublyLinkedList {
    constructor() {
        this.head = null;
        this.tail = null;
    }

    // Add a node to the end of the list
    append(value) {
        const newNode = new Node(value);

        if (!this.head) {
            // If the list is empty, set both head and tail to the new node
            this.head = newNode;
            this.tail = newNode;
        } else {
            // Link the new node to the current tail
            this.tail.next = newNode;
            newNode.prev = this.tail;
            // Update the tail to the new node
            this.tail = newNode;
        }
    }

    // Add a node to the beginning of the list
    prepend(value) {
        const newNode = new Node(value);

        if (!this.head) {
            // If the list is empty, set both head and tail to the new node
            this.head = newNode;
            this.tail = newNode;
        } else {
            // Link the new node to the current head
            newNode.next = this.head;
            this.head.prev = newNode;
            // Update the head to the new node
            this.head = newNode;
        }
    }

    // Remove a node from the list
    remove(value) {
        if (!this.head) {
            return null;
        }

        let currentNode = this.head;

        while (currentNode) {
            if (currentNode.value === value) {
                if (currentNode === this.head && currentNode === this.tail) {
                    // If it's the only node in the list
                    this.head = null;
                    this.tail = null;
                } else if (currentNode === this.head) {
                    // If it's the head node
                    this.head = currentNode.next;
                    this.head.prev = null;
                } else if (currentNode === this.tail) {
                    // If it's the tail node
                    this.tail = currentNode.prev;
                    this.tail.next = null;
                } else {
                    // If it's a middle node
                    currentNode.prev.next = currentNode.next;
                    currentNode.next.prev = currentNode.prev;
                }
                return currentNode.value;
            }
            currentNode = currentNode.next;
        }
        return null;
    }

    // Traverse the list forward
    traverseForward() {
        let currentNode = this.head;
        while (currentNode) {
            console.log(currentNode.value);
            currentNode = currentNode.next;
        }
    }

    // Traverse the list backward
    traverseBackward() {
        let currentNode = this.tail;
        while (currentNode) {
            console.log(currentNode.value);
            currentNode = currentNode.prev;
        }
    }
}

```