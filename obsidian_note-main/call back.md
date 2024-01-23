

- <span style="color:#00b0f0">A function that is passed as an argument to another function and is intended to be executed later.</span>
- Callbacks are often used to handle asynchronous operations, such as waiting for a network request to complete or responding to user interactions.
- They allow you to define what should happen after a certain task is finished.



---------------------------------------------------

```js
function doSomethingAsync(callback) {
  setTimeout(function() {
    console.log("Async task completed");
    callback(); // Call the callback function
  }, 1000); // Simulate an asynchronous operation that takes 1 second
}

function onComplete() {
  console.log("Callback function executed");
}

doSomethingAsync(onComplete);

```

------------------------------------

```js
function x(r){
  console.log('inner of x ')
  r();
}


x(function(){

    console.log('hi its anonimus ' )

})
```

- the [[setTimeout]] is actually a call back 

-  this also call back 

![[Pasted image 20230809214041.png|243]]


# <span style="color:#00b0f0">Use of call back</span> 

-  payment system of applications 



![[Pasted image 20230810153331.png|325]]



 
## <span style="color:#ff0000">demerit of call back </span>


⚙️[[call back hell]] 
 - it's unreadable and unmaintainable
⚙️ inversion of control 

			we loos the control of the code 
------------------------
			 we don t have any call back function (so we don't know wether it is work or not )

_____________________
			⤵️
#a_project_with_all_thing-- 

___________________________
12*