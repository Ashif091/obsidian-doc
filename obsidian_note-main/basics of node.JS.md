- create a basic server 
  ![[Pasted image 20230817151655.png|300]]

- Fs module (File System) [[Fs module]]

  
```js
  
The `fs` module in Node.js, short for "File System," provides an interface for interacting with the file system on your computer.

```

- inside the `else` block (when there is no error reading the file), I've added `res.write(data.toString());`. The `data` variable returned by `fs.readFile` is a `Buffer`, and the `res.write()` function expects a string or a buffer as an argument. By using `.toString()`, we convert the buffer to a string before writing it to the response.
- 
![[Pasted image 20230817161743.png|400]]
## work out method 
```js
let http = require('http')

let fs = require('fs')

http.createServer(function(req,res){

  fs.readFile("./work/index.html",function(err,data){

    if(err){

      res.writeHead(500,{'Content-Type':'text/plain'})

      res.end('WARNIG IT WILL EXPLODE IN 4S ')

    }

    else{

      res.writeHead(200,{'Content-Type':'text/html'})

      res.write(data.toString());

      res.end()

    }

  })

}).listen(3000)
```

- if you use form submition there problem when u use url like this ⤴️ so there is alternative way for this that is the use of <span style="color:#00b0f0">url module </span>exp⤵️

```js
let http = require('http')

let fs = require('fs')

let url = require('url')

http.createServer(function(req,res){

  let info =url.parse(req.url)

  if(info.pathname==='/'){

     fs.readFile("./work/index.html",function(err,data){

    if(err){

      res.writeHead(500,{'Content-Type':'text/plain'})

      res.end('WARNIG IT WILL EXPLODE IN 4S ')

    }

    else{

      res.writeHead(200,{'Content-Type':'text/html'})

      res.write(data.toString());

      res.end()

    }

  })

  }

  else if(info.pathname==='/login'){

    res.write('already logined')

    res.end()

  }

  else{

    res.write('erorr 343')

    res.end()

  }

  

}).listen(3000,function(){

  console.log("start")

})
```

![[Pasted image 20230820111440.png|375]]












id=13