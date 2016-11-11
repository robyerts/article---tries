A **Trie** is a tree data structure used for fast look-ups of strings. At a slightly higher memory cost, the Trie allows for searching, inserting, deleting in O(L), where L is the key length.   
Special with Tries, you can quicly look-up prefixes, determine longest common prefixes between words, and even generate suggestions of words.
(...compare it to hash table more  ? ...)
**Tries are NOT implemented in the standard library**

In a **Trie** , each node stores a *Character* and can point to the next *Character*/Node in the sequence. 

The following is a representation of a Trie containing the words : round, roll, to, tour. Notice the **value** and **nrOfInstances** notations.


![TRIE](https://raw.githubusercontent.com/robyerts/article---tries/master/TRIE.png)
The **root** node keeps everything connected; 
**value** is a *Character* while 
**nrOfInstances** is an *Int* representing the number of times that node is being used. **root** doesn't contain a *Character*, therefore, it is not actually part of any sequence. It will all make sense after a few examples :)

#### Insert
(...to be continued...)

(..not so appropiate.)
On the left branch we have the words "roll" and "round". Their common prefix is "ro". The nodes corresponding to those letters  have their **nrOfInstances** = 2, while the rest have **nrOfInstances** = 1 .(...)


In my implementation the class **Node** is defined by the following members :
```swift
class Node {
	var value: Character?
	var father: Node?
	var chids: [Node]   
	var nrOfInstances: Int
}
```

