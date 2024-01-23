  
The `bind()` and `call()` methods in JavaScript both serve the purpose of setting the `this` value for a function, but they have some differences in how they achieve that and when they're used.

- **`bind()`**: The `bind()` method returns a new function with the specified `this` value, but it does not immediately invoke the function. You can store this new function and call it later whenever you want.
- **`call()`**: The `call()` method immediately invokes the function with the specified `this` value and the provided arguments. It doesn't return a new function; it directly executes the function.
![[Pasted image 20230811193756.png]]
```js
const person = {
  firstName: "John",
  lastName: "Doe",
  getFullName: function() {
    return this.firstName + " " + this.lastName;
  }
};

const fullNameFunction = person.getFullName;
console.log(fullNameFunction()); // This would give an error because "this" inside the function is not the person object

const boundFullNameFunction = person.getFullName.bind(person);
console.log(boundFullNameFunction()); // This works as "this" is explicitly set to the person object

```

# Simple example of a call 


```js
let user = {

    fristname : 'ashif ',
    lastname : 'ali',
    printfullname : function gx  (){
        console.log ( this.fristname +''+ this.lastname  );
    }
}  

 let neWser = {
    fristname : 'muhammed ',
   lastname : 'adil'
 }
 user.printfullname.call(neWser);
```

_____________________________________________________________________

			 it can change like that 



___________________________

## Advanced exp 
```js
const person = {
  firstName: "John",
  lastName: "Doe",
  getFullName: function() {
    return this.firstName + " " + this.lastName;
  }
};

function greet(greeting) {
  return greeting + " " + this.getFullName();
}

const result = greet.call(person, "Hello");
console.log(result); // Outputs: "Hello John Doe"

```

----------------

#a_project_with_all_thing--

```js
let user = {

    fristname : 'ashif ',

    lastname : 'ali',

}

let printfullname =  function gx  ( gw){

    console.log ( this.fristname +''+ this.lastname + ' ' +gw );

  

}

  

 let neWser = {

    fristname : 'muhammed ',

    lastname : 'adil'

 }

   let asq;

  
  

passer(1)

.then(function(id){

    printfullname.call(id,'age is unknown ');

})

.catch(function(err){

    console.log(err);

})

  
  

function passer(num){

    const compalar = new Promise ( (resolve , reject )=>{

        if(num ==2|num ==1){

             let result =checker(num);

             resolve ( result );

        }

        else{

            let err = new Error ('fake id')

            reject(err);

        }

    } )

    return compalar;

}

  

function checker (num){

   if(num==1){

    return neWser;

   }

   else{

    return user;

   }

}
```

---------------------









12*