- <span style="color:#00b0f0">Constructors are typically used in object-oriented programming to define a blueprint for creating instances of a particular type or class of objects.
</span>





```js
 Constructor function for creating Person objects

function Person(name, age) {

    this.name = name;

    this.age = age;

}

  

// Adding a method to the prototype of Person

Person.prototype.sayHello = function() {

    console.log(`Hello, my name is ${this.name} and I'm ${this.age} years old.`);

};

  

// Creating two Person objects

const person1 = new Person('Alice', 30);

const person2 = new Person('Bob', 25);

  

// Calling the method inherited from the prototype

person1.sayHello(); // Output: Hello, my name is Alice and I'm 30 years old.

person2.sayHello(); // Output: Hello, my name is Bob and I'm 25 years old.
```


page id =  293734