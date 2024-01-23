- <span style="color:#00b0f0"> promise is an object representing the eventual completion or failure of an asynchronous operation</span>

- They help in avoiding callback hell and make code more readable and maintainable.

- Promise chaining (attached with a call back function)

<span style="color:#ffff00">Promises have three states</span>:

1. **<span style="color:#51f0d0">Pending</span>**: The initial state. The promise is neither fulfilled nor rejected.
    
2. **<span style="color:#51f0d0">Fulfilled</span>**: The asynchronous operation completed successfully, and the promise has a resulting value.
    
3. **<span style="color:#51f0d0">Rejected</span>**: The asynchronous operation encountered an error or failure, and the promise holds the reason for the failure.

an exp : 

```js
// Function to fetch data from an API using a Promise
function fetchData() {
  return new Promise((resolve, reject) => {
    fetch('https://jsonplaceholder.typicode.com/posts/1')
      .then(response => {
        if (!response.ok) {
          throw new Error('Network response was not ok');
        }
        return response.json();
      })
      .then(data => {
        resolve(data);
      })
      .catch(error => {
        reject(error);
      });
  });
}

// Using the fetchData function with Promises
fetchData()
  .then(data => {
    console.log('Fetched data:', data);
  })
  .catch(error => {
    console.error('Error fetching data:', error);
  });

```

---------------

## promise.race

```js
const promise1 = new Promise((resolve, reject) => {
    setTimeout(resolve, 100, 'Promise 1 resolved');
});

const promise2 = new Promise((resolve, reject) => {
    setTimeout(resolve, 200, 'Promise 2 resolved');
});

const promise3 = new Promise((resolve, reject) => {
    setTimeout(reject, 150, 'Promise 3 rejected');
});

const racePromise = Promise.race([promise1, promise2, promise3]);

racePromise
    .then(result => {
        console.log('Fulfilled:', result);
    })
    .catch(error => {
        console.log('Rejected:', error);
    });


```
-----------------------
### prommise.all
```js
const promise1 = new Promise((resolve, reject) => {
    setTimeout(resolve, 100, 'Promise 1 resolved');
});

const promise2 = new Promise((resolve, reject) => {
    setTimeout(resolve, 200, 'Promise 2 resolved');
});

const promise3 = new Promise((resolve, reject) => {
    setTimeout(resolve, 150, 'Promise 3 resolved');
});

const allPromise = Promise.all([promise1, promise2, promise3]);

allPromise
    .then(results => {
        console.log('All promises resolved:', results);
    })
    .catch(error => {
        console.log('At least one promise rejected:', error);
    });

```

- <span style="color:#00b0f0">Since all promises resolve without any rejections, the `then` block will be executed, and the `results` array will contain the resolved values from all three promises.</span>

_______________________
### promise.any

```js
const promise1 = new Promise((resolve, reject) => {
    setTimeout(reject, 200, 'Promise 1 rejected');
});

const promise2 = new Promise((resolve, reject) => {
    setTimeout(resolve, 100, 'Promise 2 resolved');
});

const promise3 = new Promise((resolve, reject) => {
    setTimeout(resolve, 150, 'Promise 3 resolved');
});

const anyPromise = Promise.any([promise1, promise2, promise3]);

anyPromise
    .then(result => {
        console.log('At least one promise fulfilled:', result);
    })
    .catch(errors => {
        console.log('All promises rejected:', errors);
    });

```

- 

____________


 ## video reference 

```js
const cart = ["laptop " , " pc ", " gun "]
const promise =  order(cart);
console.log(promise)
promise.then (function (user) {
    console.log(user);
})
.catch(function(err){ // to handle the error

    console.log(err.message)

})

  
function order(cart){
    const or = new Promise (function (resolve , reject ){
        if(!payment(cart)){
            const err = new Error ('network error ')
            reject (err)
        }
        const user = 123344;
        if(user){
            setTimeout(function(){
                resolve (user)
            },1000)
        }
    })
    return or ;
}
function payment(){

    return true ;

}
```

- we can pass the data from one level to another level (promise chain )
- by use the then method 
 


![[Pasted image 20230810220400.png|450]]

----------------------------------
![[Pasted image 20230810220420.png|525]]
______________________________


-  it is simply attaching a function 



![[Pasted image 20230810194904.png|325]]

## another example  for this with practical know loge 

```js
const cart = 
	  ["laptop " , " pc ", " gun "]

const promise =  order(cart);

console.log(promise)

promise.then (function (user) {

    console.log(user);

    return user;

})

  

.then(function (user){

     payment( user)

     .then ( function ( user ){

        console.log(user)

  

     })

})

.catch(function(err){

    console.log(err.message)

})

  

function order(cart){

    const or = new Promise ( (resolve , reject )=>{

        if(!paytm(cart)){

            const err = new Error ('network error ')

            reject (err)

        }

        const user = 123344;

        if(user){

            setTimeout(function(){

                resolve (user)

  

            },1000)

        }

  

    })

    return or ;

  

}

function paytm(cart){

    return true;

}

  

function payment(user ){

     const pay = new Promise (function (resolve , reject ){

        resolve ( 'payment succesfull  '+'id = ' + user  );

        reject ( 'oops')

     })

     return pay ;

}
```



# Advanced one ( own creation )

```js
let user = {

    fristname : 'ashif ',

    lastname : 'ali',

}

let printfullname =  function gx  (){

    console.log ( this.fristname +''+ this.lastname  );

  

}

  

 let neWser = {

    fristname : 'muhammed ',

    lastname : 'adil'

 }

   let asq;

  
  

passer(1)

.then(function(id){

    printfullname.call(id);

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


_________________________________


# __________________________________


#a_project_with_all_thing-- 


12*