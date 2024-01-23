### <span style="color:#ffff00">basic exp</span> 
```js
function x(){

     setTimeout (function(){

    console.log('hello')

     },1000);

     console.log('hi')

}

x();
```

		it store the data away from call stack when it run it wil return in to call stack
 
 #web_api
 
#### ? print 12345 with the cap of that time
![[Pasted image 20230809125220.png|300]]
`there is problem with that `
`in the time  of code run - the settimeout will wite for the time but loop is run out so i become  6 `


			out is 6 6 6 6 6 

- if here we use let then out is 

		out is 1 2 3 4 5 


-  it becomes the let have every reference of i in the block scop of let


### <span style="color:#ffff00"> can fix this problem in the case of var
</span>



```js


function x(){

    for( var  i=1 ; i<=5 ; i++){

      function c(i){

         setTimeout (function(){

       console.log(i);

      },1000);

      }  

      c(i);

       console.log('out ' + i)  
    }
}

x();

```



		 we are passing the value ( i ) to anathor funtion  
		 due to this we get each storage for it 



### they can wait for the 

![[Pasted image 20230810110901.png]]


----------------
page id =  293734