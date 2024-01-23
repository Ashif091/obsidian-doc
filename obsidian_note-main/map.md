In JavaScript, the `map` <span style="color:#00b0f0">function is used to transform elements of an array into a new array by applying a given function to each element</span>. It's a higher-order function that takes a callback function as an argument and returns a new array with the results of applying the callback to each element of the original array.



```js
let rst = [12,3,34,54,5];

const pkr =rst.map(n => {

       return n<30;

  

});

console.log(pkr);
```


exp 
```js 
let arry = [12,43,55,645,5]

function double (x){

   return 2*x ;

}

let arry2 =  arry.map ( double )

console.log ( arry2);  

let arru3 = arry. map((x)=>{

    return 3*x ;
})

console.log( arru3);
```












12*