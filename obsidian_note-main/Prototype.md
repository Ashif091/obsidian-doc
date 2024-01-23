
- <span style="color:#00b0f0">In JavaScript, a prototype is an inherent mechanism that allows objects to inherit properties and methods from other objects</span>
- Every object in JavaScript has a prototype, which serves as a blueprint for that object's properties and behaviors.
 ````js
 // Constructor function
function Person(name, age) {
    this.name = name;
    this.age = age;
}

// Adding a method to the prototype of Person
Person.prototype.sayHello = function() {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
};

// Creating objects using the Person constructor
const person1 = new Person('Alice', 25);
const person2 = new Person('Bob', 30);

person1.sayHello();  // Output: Hello, my name is Alice and I am 25 years old.
person2.sayHello();  // Output: Hello, my name is Bob and I am 30 years old.

````



```js
let x = {
    name: 'ashif ',
    place: 'malappuram ',
    fun:function(){console.log(this.name +'from '+ this.place  )}
}

let s ={
    name : 'anfas'
    ,age : 12
}
x.prototype  = s;
x.fun();
```
___________
```js 


```


![[Pasted image 20230811205353.png|375]]

out print 
![[Pasted image 20230811205619.png|301]]


















12*