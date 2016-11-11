A Trie is a tree data structure used for fast look-ups of strings. At a slightly higher memory cost, the Trie allows for searching, inserting, deleting in O(L), where L is the key length .(...compare it to hash table ...)

In a Trie , each node stores a character, but the node itself is not identifible only by that, but by the entire path .

The following is a representation of a trie containing the words : round, roll, to, tour. Notice the **value** and **nrOfInstances** notations .


![TRIE](https://raw.githubusercontent.com/robyerts/article---tries/master/TRIE.png)



In my implementation the class **Node** is defined by the following members :
```swift
class Node {
	var value: Character?
	var father: Node?
	var chids: [Node]   
	var nrOfInstances: Int
}
```
