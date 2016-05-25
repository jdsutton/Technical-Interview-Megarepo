# Data Structures

## Arrays

| Operation                  | Time Complexity    |
|----------------------------|--------------------|
| Access                     | Θ(1)               |
| Insert/delete at beginning | N/A                |
| Insert/delete at end       | N/A                |
| Insert/delete in middle    | N/A                |
| Wasted space (average)     | 0                  |

## Dynamic Arrays

| Operation                  | Time Complexity    |
|----------------------------|--------------------|
| Access                     | Θ(1)               |
| Insert/delete at beginning | Θ(n)               |
| Insert/delete at end       | Θ(1) (amortized)   |
| Insert/delete in middle    | Θ(n)               |
| Wasted space (average)     | Θ(n)               |

## Linked Lists
* [Linked List Visualization](http://visualgo.net/list)
* [Cycle Finding Visualization](http://visualgo.net/cyclefinding)

| Operation                  | Time Complexity    |
|----------------------------|--------------------|
| Access                     | Θ(n)               |
| Insert/delete at beginning | Θ(1)               |
| Insert/delete at end       | Θ(1)               |
| Insert/delete in middle    | search time + Θ(1) |
| Wasted space (average)     | Θ(n)               |

## Binary Heaps
* [Heap Visualization](http://visualgo.net/heap)
* Useful for quickly finding the minimum or maximum of a set of values
* Useful for sorting values (heapsort)

| Operation    | Time Complexity    |
|--------------|--------------------|
| Find min     | Θ(1)               |
| Delete min   | Θ(log n)           |
| Insert       | Θ(log n)           |
| Decrease Key | Θ(log n)           |
| Merge        | Θ(n)               |

## Stacks
* TODO

## Queues
* TODO

## Trees
* TODO

## Binary Trees
* [Binary Tree Visualization](http://kanaka.github.io/rbt_cfs/trees.html)
* Can be stored in an array without using pointers
  * Inefficient for sparse trees

## N-ary Trees
* [Wikipedia - K-ary tree](https://en.wikipedia.org/wiki/K-ary_tree)
* Rooted tree where each node has at most N children
* Binary tree is a special case where N = 2
* For an N-ary tree of height h, the maximum number of leaves is N<sup>h</sup>
* Can be stored in an array
  * c<sup>th</sup> child: child(i, c) = k * i + c
  * parent(i) = floor((i - 1) / k)

## Binary Search Trees
* [Binary Search Tree Visualization](http://visualgo.net/bst)

## Balanced Binary Search Trees
* TODO
* AVL Tree
* Splay Tree
* Red-Black Tree

## Trie-Trees
* [Trie Visualization](https://people.ok.ubc.ca/ylucet/DS/Trie.html)
* [Wikipedia - Trie](https://en.wikipedia.org/wiki/Trie)
* "In computer science, a trie, also called digital tree and sometimes radix tree or prefix tree (as they can be searched by prefixes), is an ordered tree data structure that is used to store a dynamic set or associative array where the keys are usually strings. Unlike a binary search tree, no node in the tree stores the key associated with that node; instead, its position in the tree defines the key with which it is associated. All the descendants of a node have a common prefix of the string associated with that node, and the root is associated with the empty string"
* Useful for searching by prefix among stings with lots of overlap
* Possible dictionary implementation

## Graphs
* [Graph Visualization](http://visualgo.net/graphds)
* TODO

## HashTables
* [HashTable Visualization](http://visualgo.net/hashtable)
* Useful for very fast lookup, insertion, deletion
* Common implementation of a dictionary

|Operation| Average | Worse Case |
|---------|---------|------------|
| Space   | O(n)    | O(n)       |
| Search  | O(1)    | O(n)       |
| Insert  | O(1)    | O(n)       |
| Delete  | O(1)    | O(n)       |

## Union-find
* [Union-find Visualization](http://visualgo.net/ufds)
* Useful for quickly determining if two items belong to the same set
* Useful for quickly joining sets
* [Wikipedia - Disjoint-set data structure](https://en.wikipedia.org/wiki/Disjoint-set_data_structure)
* "...the amortized time per operation is only O(α(n)) ... Thus, the amortized running time per operation is effectively a small constant."
