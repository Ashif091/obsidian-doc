
- <span style="color:#ff0000">block is compound of statement </span>
```js
{
var d = 'dkfj';
console.log(d)
}
``` 
-  if u want to write a multiple line for a function or something <span style="color:#00b0f0">then must use block </span>

### BLOCK scope  
- Block scope is a concept in programming languages where variables declared inside a block of code,
- only accessible within that block and any nested blocks
#block 

### Shadowing JS 
	shadowing is reassing the value 
Because the var is a global variable                                                                     #shadowing
```js
var x = 100;
{
var x = 21;
let a = 1;
const b = 2;
// here all veriable have access 
}
`here only var `
 console.log(x) `21` // becouse it shadowing 
```

#### legal shadowing 
```js
var x =100;
{
 let x = 12;
 
}
```
#### illegal shadowing 
```js
let  x =100;
{
 var x = 12;
 
}
```



![[Pasted image 20230808141504.png|167]]
out put is ` 200`






---------------
page id =  293734