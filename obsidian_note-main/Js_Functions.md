```js
a(); // it will create a execution context  and pull into the call stack   
b();  // it will create another execution context
🔸`here the function is inwalked `
var x = 1;
console.log(x)  
function a(){ //tis is a block ⤵️
    var x = 12;
    console.log(x);
}
function b(){
    var x = 14;
    console.log(x);
}
```
		out {
		12-14-1
		}
[[Code execution]] #execution_context   [[block]]
		when execution is over then all call stack memory is gone 

 
   
   ![[Pasted image 20230808003402.png|500]]
 ## If u run empty code it will create a execution context 
 
 JS engine and window(JS engine code in windows)
 - also create the this memory space
- [[This]] memory 
- #global_space any is not inside of the function
- we can call ver like this
 
![[Pasted image 20230808102203.png|206]]


## type of functions 

[[type of function]]




## DATE  calculations by JS function (code work on 8823)
```js
function dayCalcu(enddate,startdate){
    const end = new Date (enddate);
    const start = new Date (startdate);
    const day = 24*60*60*1000;
    const timedf = Math.abs(end - start);
    const daydf =Math.floor(timedf/day)
    return daydf;
}
const days = dayCalcu('2003-12-02','2023-08-08' );
console.log(days);
```



#defult_parameter
![[Pasted image 20230817132215.png|225]]












#### Video reference
<iframe width="560" height="315" src="https://www.youtube.com/embed/gSDncyuGw0s" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>page id =  293734