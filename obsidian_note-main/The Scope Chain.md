### Lexical Environment
```js 
a();
function a(){
 b();
 var g =19
 function b(){
   console.log(x);
 }
}
```
		 here b is Lexicaly located in a function 

![[Pasted image 20230808114027.png|500]]
		**The "scope chain" in JavaScript is the sequence of nested levels of code, known as "lexical environments," where the JavaScript engine searches for variables and identifiers. Each lexical environment contains its own set of variables and identifiers. Starting from the current location, the engine looks outward through these nested environments, including containing functions and the global [[scope]]. This chain of lexical environments determines where variables can be found and accessed within your code.**





-------------
page id =  293734