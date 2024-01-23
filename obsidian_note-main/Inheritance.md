```js
  

class sample {

  xrp(){

    console.log('hi iam ');

  }

  

}

  

class x extends sample {

     constructor(name,age ){

        super();

        this.name= name;

        this.age = age

  

     }

     fun () {

        console.log(`your name is ${this.name}`)

     }

  

}

  

let xclass = new x ('ashif','12');

xclass.fun();

xclass.xrp();
```
12*