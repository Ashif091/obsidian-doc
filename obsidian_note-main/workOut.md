
		 what about  the output 



```js
var data=  [

    {
        name : 'one ',

        msg : 'hi i am one'
    }   ,
   {
     name : 'two ',
   msg : 'hi i am two'

    },
    {

        name : 'three',

        msg : 'hi i am three'

    }

];

  

function  xs(){

     data.forEach( (item)=>{

    const bt = document.createElement('button');

    bt.innerHTML = item.name;

    bt.onclick = msgp(item.msg);

    document.body.appendChild(bt)

  
  

   });

}

xs();

function msgp(arg){

    alert(arg)

}

```




page id =  293734