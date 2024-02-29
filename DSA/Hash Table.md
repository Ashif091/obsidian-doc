- A hash table, also known as hash map, is a data structure that is used to store key-value pairs
- Given a key, you can associate a value with that key for very fast lookup
- JavaScript's Object is a special implementation of the hash table data structure. However, Object class adds its own keys. Keys that you input may conflict and overwrite the inherited default properties
- Maps which were introduced in 2015 allow you to store key-value pairs
- Writing your own hash table implementation is a very popular JavaScript interview question

﻿

## Hash Table contd.
___
- We store the key value pairs in a fix sized array
- Arrays have a numeric index
- How do we go from using a string as an index to number as an index?
- A hashing function accepts the string key, converts it into a hash code using a defined logic and then maps it into a numeric index that is within the bounds of the array
- Using the index, store the value
- The same hashing function is reused to retrieve the value given a key
___
## Methods in Hash Table
_______________________
- Set to store a key-value pair
- Get to retrieve a value given its key Remove to delete a key value pair
- Remove to delete a key value pair
__________________________________________
![[Pasted image 20240216095609.png]]

___
﻿

## Hash Table Usage
- Hash tables are typically implemented where constant time lookup and insertion
- are required
- Database indexing
- Caches

____
## **Separate Chaining**
____
```js
class HashTable {
  constructor() {
    this.table = new Array(127);
    this.size = 0;
  }

  _hash(key) {
    let hash = 0;
    for (let i = 0; i < key.length; i++) {
      hash += key.charCodeAt(i);
    }
    return hash % this.table.length;
  }

  set(key, value) {
    const index = this._hash(key);
    if (this.table[index]) {
      for (let i = 0; i < this.table[index].length; i++) {
        if (this.table[index][i][0] === key) {
          this.table[index][i][1] = value;
          return;
        }
      }
      this.table[index].push([key, value]);
    } else {
      this.table[index] = [];
      this.table[index].push([key, value]);
    }
    this.size++;
  }

  get(key) {
    const index = this._hash(key);
    if (this.table[index]) {
      for (let i = 0; i < this.table.length; i++) {
        if (this.table[index][i][0] === key) {
          return this.table[index][i][1];
        }
      }
    }
    return undefined;
  }

  remove(key) {
    const index = this._hash(key);

    if (this.table[index] && this.table[index].length) {
      for (let i = 0; i < this.table.length; i++) {
        if (this.table[index][i][0] === key) {
          this.table[index].splice(i, 1);
          this.size--;
          return true;
        }
      }
    } else {
      return false;
    }
  }

  display() {
    this.table.forEach((values, index) => {
      const chainedValues = values.map(
        ([key, value]) => `[ ${key}: ${value} ]`
      );
      console.log(`${index}: ${chainedValues}`);
    });
  }
}
```

___




```js
class HashTable {
  constructor(size) {
    this.table = new Array(size);
    this.size = size;
  }

  hash(key) {
    let total = 0;
    for (let i = 0; i < key.length; i++) {
      total += key.charCodeAt(i);
    }
    return total % this.size;
  }

  set(key, value) {
    const index = this.hash(key);
    const bucket = this.table[index];
    if (!bucket) {
      this.table[index] = [[key, value]];
    } else {
      const sameKeyItem = bucket.find((item) => item[0] === key);
      if (sameKeyItem) {
        sameKeyItem[1] = value;
      } else {
        bucket.push([key, value]);
      }
    }
  }

  get(key) {
    const index = this.hash(key);
    const bucket = this.table[index];
    if (bucket) {
      const sameKeyItem = bucket.find((item) => item[0] === key);
      if (sameKeyItem) {
        return sameKeyItem[1];
      }
    }
    return undefined;
  }

  remove(key) {
    let index = this.hash(key);
    const bucket = this.table[index];
    if (bucket) {
      const sameKeyItem = bucket.find((item) => item[0] === key);
      if (sameKeyItem) {
        bucket.splice(bucket.indexOf(sameKeyItem), 1);
      }
    }
  }

  display() {
    for (let i = 0; i < this.table.length; i++) {
      if (this.table[i]) {
        console.log(i, this.table[i]);
      }
    }
  }
}

const table = new HashTable(10);
table.set("name", "Bruce");
table.set("age", 25);
table.display();
console.log(table.get("name"));
table.set("mane", "Clark");
table.set("name", "Diana");
console.log(table.get("mane"));
table.remove("name");
table.display();

```

##  Linear Probing

```js
class HashTable {
    constructor() {
        this.table = [];
    }

    modularHash(key) {
        let sum =  0;
        for (let i =  0; i < key.length; ++i) {
            sum += key.charCodeAt(i);
        }
        let hash = sum %  71;  
        return hash;
    }

    put(key, value) {
        let hash = this.modularHash(key);
        if (this.table[hash] === undefined) {
            return this.table[hash] = [key, value];
        } else {
            while (this.table[hash] !== undefined) {
                hash++;
            }
        }
        return this.table[hash] = [key, value];
    }

    get(key) {
        let hash = this.modularHash(key);
        while (this.table[hash] !== undefined) {
            if (this.table[hash][0] === key) {
                return this.table[hash][1];
            }
            hash++;
        }
        return undefined;
    }
}

```

## Array duplicate count by using HT

```js
class hashTable{
    constructor(capacity){
        this.table = new Array(capacity)
        this.size = 0
    }
    hash(key){
        let hash = 0
        for (let i = 0; i < key.length; i++) {
            hash += key.charCodeAt(i)            
        }
        return hash % this.table.length
    }
    set(key,value){
        let index = this.hash(key)
        if(this.table[index]){
            for (let i = 0; i < this.table[index].length; i++) {
                if(this.table[index][i][0]===key){
                    this.table[index][i][1]=value
                    return ;
                }
                this.table[index].push([key,value])
            }
        }else{
            this.table[index] = []
            this.table[index].push([key,value])
        }
        this.size++
        return ;
    }
    get(key){
        let index = this.hash(key)
        if(this.table[index] && this.table[index].length){
            for (let i = 0; i < this.table[index].length; i++) {
                if(this.table[index][i][0]===key){
                    return this.table[index][i][1]
                }
            
        }
        return null
    }
    display(){
        this.table.forEach((bucket,index)=>{
            let data = bucket.map(([key,value])=>{
                return `[${key}:${value}]`
            })
            console.log(`${index}:{${data}}`);
        })
    }
}

let table = new hashTable(50)

let arr = ['A','D','S','A','A','D','S','F','F','D']
function arrToTable(arr){
    for (let i = 0; i < arr.length; i++) {
        if(table.get(arr[i])===null){
            table.set(arr[i],1)
        }else{
            table.set(arr[i],(table.get(arr[i])+1))
        }
    }
}
arrToTable(arr)
table.display()
```
