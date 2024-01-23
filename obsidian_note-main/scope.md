**Scopes determine where a particular variable or function can be accessed and modified in your code**
1. **Global Scope:** Variables declared outside of any function or code block have global scope. They can be accessed from any part of the code, including within functions and nested code blocks.
    
    javascriptCopy code
    ```js
    let globalVar = 10;  function myFunction() {   console.log(globalVar); // Accessible, outputs: 10 }`
```
    
    
### 2. **Local Scope:**
Variables declared inside a function or code block have local scope. They are only accessible within that function or block and its nested blocks.
    
    javascriptCopy code
    
    `function myFunction() {   let localVar = 5; // Local to myFunction   console.log(localVar); // Accessible, outputs: 5 }  console.log(localVar); // Not accessible, results in an error`




---------------
page id =  293734