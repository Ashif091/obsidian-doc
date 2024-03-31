- Trie , also known as a prefix tree, is a tree-like data structure used to store a collection of strings.
- Each node represents a character, and each path from the root to a node represents a string in the collection. 
- Tries are efficient for searching for strings with common prefixes.


 Applications
 ____
- Spell Checker
- Auto-Complete
- Browser History

___
### Advantages

- Insert and search faster than hash tables and BST
- Provides alphabetical filter of entries by the key of the node
### Disadvantages

- Requires more memory to store the strings
- Slower than hash tables.
Copy

```javascript
class TrieNode {
	constructor() {
		this.children = {};
		this.isEndOfWord = false;
	}
}

class Trie {
	constructor() {
		this.root = new TrieNode();
	}

	// Below Functions goes here
}
```
### Basic Operations
### Insertion
```javascript
insert(word) {
	let curr = this.root;
	for(let char of word) {
		if(!curr.children[char]) {
			curr.children[char] = new TrieNode ();
		}
		curr = curr.children[char];
	}
	curr.isEndOfWord = true;
}
```

#### Search

Copy

```javascript
search(word) {
	let node = this.root;
	for(let char of word) {
		if(!node.children[char]) {
			return false;
		}
		node = node.children[char];
	}
	return node.isEndOfWord;
}
```

‣

### Print Words as a array

Copy

```javascript
printWords(node = this.root, currentWord = "", result = []) {
	if(node.isEndOfWord) {
		result.push(currentWord);
	}

	for(let char in node.children) {
		this.printWords(node.children[char], currentWord + char, result);
	}
	return result;
}


let trie = new TrieNode()
log(trie.printWords())
```

‣

### Auto Complete

Copy

```javascript
autoComplete(word) {
    let node = this.root;
    for (let char of word) {
      if (!node.children[char]) {
        return [];
      }
      node = node.children[char];
    }
    let list = [];
    this.collectWord(node, word, list);
    return list;
  }

  collectWord(node, word, list) {
    if (node.isEndOfWord) {
      list.push(word);
    }

    for (let char in node.children) {
      this.collectWord(node.children[char], word + char, list);
    }
  }
```






