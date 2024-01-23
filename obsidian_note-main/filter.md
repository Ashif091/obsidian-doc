
  
Filtering in JavaScript refers to<span style="color:#00b0f0"> the process of selecting specific elements from an array based on a certain condition.</span> The `filter()` method is commonly used to achieve this. It creates a new array containing all elements that pass the specified condition.

Here's a simple example of using the `filter()` method in JavaScript:
```js
// Original array of numbers
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

// Filtering even numbers
const evenNumbers = numbers.filter(number => number % 2 === 0);

console.log(evenNumbers); // Output: [2, 4, 6, 8, 10]

```

```js
let arry = [12,43,55,645,5] 

let divisibleOfTwo = arry.filter(function ( x ){
  return x%2==0;
})
 
let divisibleOf5 = arry.filter (  (x)=>{
    return x%5==0 ;
} )

console.log(divisibleOf5)
```


```js
let rst = [12,3,34,54,5];

const pkr =rst.filter(n => {

       return n<30;

  

});

console.log(pkr);
```




# advanced exp of filter  and [[map]]
```js
const data = [

    {user : ' ashifali ' , age : 19 },

    {user : ' anfas  ' , age : 49 },

    {user : ' nithin ' , age : 69 },

]

  

const agefinder = data.filter((x)=>{

    return (x.age<30) }).map((x)=>{return (x.user)})

  

console.log(agefinder);
```




#concatenatingString 12*