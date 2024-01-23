#### <span style="color:#00b0f0">closure  is a function having access to its parent scope even after the parent function closed or executed</span>
### <span style="color:#ffff00">exp simple code</span>
```js
function a(v1, v2){
    function b(){
        let x = v1 + v2 ;  >/ here create the closure:a{ v1 = 3 , v2 =4}
        return x           >/ result will save into window 
    }
   return b();
}

let sum = a(3,5);

console.log(sum)
```

### <span style="color:#ffff00">another exp </span>

```js
function a(v1, v2){
    function b(){
        let x = v1 + v2 ;
       console.log(x) 
    }
   return b ;   /here the functon will directly send the a blue print to the sum ver
}

let sum = a(3,5);
sum(); / creat a exicution context for the function b &  closure will create and v1= 3 v2 = 5 

```


### <span style="color:#ffff00"> use case of closure </span>
 [[call back]]  from the code
 ```js
 var data=  [

    {
        name : 'one ',
        msg : 'hi i am one'
    }  ,
    {
        name : 'two ',
        msg : 'hi i am two' 
    }    ,
    {
       name : 'three',
        msg : 'hi i am three'
  
    }
];
  
function  xs(){

   data.forEach( (item)=>{
    const bt = document.createElement('button');
    bt.innerHTML = item.name;
    bt.onclick = msgp;
    document.body.appendChild(bt)
   });
}
xs();
function msgp(){        `here we can't tell the matter of msg in it becorse it is call back ( in call can,t pass the DATA ⤴ arrgument  )`
    alert('hi')
}
```

#### use exp 
```js
var data=  [

    {

        name : 'one ',

        msg : 'hi i am one'

    }

    ,

    {

        name : 'two ',

        msg : 'hi i am two'

  

    }

    ,

    {

        name : 'three',

        msg : 'hi i am three'

  

    }

];

  

function  xs(){

     data.forEach( (item)=>{

    const bt = document.createElement('button');

    bt.innerHTML = item.name;

    bt.onclick = rgt(item.msg); `there is assgranus working`  

    document.body.appendChild(bt)

  
  

   });

}

xs();

function rgt(arg){

    function mst (){

    alert(arg)

}

return mst;

}

```
[[Js_Functions]]

- if need any extra memory u can use closure 














12*