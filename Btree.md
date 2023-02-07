### Properties of B-Tree: 
1. All leaves are at the same level.
2. B-Tree is defined by the term minimum degree ‘t‘. The value of ‘t‘ depends upon disk block size.
3. Every node except the root must contain at least t-1 keys. The root may contain a minimum of 1 key.
4. All nodes (including root) may contain at most (2*t – 1) keys.
5. Number of children of a node is equal to the number of keys in it plus 1.
6. All keys of a node are sorted in increasing order. The child between two keys k1 and k2 contains all keys in the range from k1 and k2.
7. B-Tree grows and shrinks from the root which is unlike Binary Search Tree. Binary Search Trees grow downward and also shrink from downward.
8. Like other balanced Binary Search Trees, the time complexity to search, insert and delete is O(log n).
9. Insertion of a Node in B-Tree happens only at Leaf Node.

### Busca

Search Operation in B-Tree: 
Search is similar to the search in Binary Search Tree. Let the key to be searched is k. 

Start from the root and recursively traverse down. 
For every visited non-leaf node, 
If the node has the key, we simply return the node. 
Otherwise, we recur down to the appropriate child (The child which is just before the first greater key) of the node. 
If we reach a leaf node and don’t find k in the leaf node, then return NULL.
Searching a B-Tree is similar to searching a binary tree. The algorithm is similar and goes with recursion. At each level, the search is optimized as if the key value is not present in the range of the parent then the key is present in another branch. As these values limit the search they are also known as limiting values or separation values. If we reach a leaf node and don’t find the desired key then it will display NULL.


### Insertion 
1. Initialize x as root. 
2. While x is not leaf, do following 
2.1. Find the child of x that is going to be traversed next. Let the child be y. 
2.2. If y is not full, change x to point to y. 
2.3. If y is full, split it and change x to point to one of the two parts of y. If k is smaller than mid key in y, then set x as the first part of y. Else second part of y. When we split y, we move a key from y to its parent x. 
3. The loop in step 2 stops when x is leaf. x must have space for 1 extra key as we have been splitting all nodes in advance. So simply insert k to x. 

Note that the algorithm follows the Cormen book. It is actually a proactive insertion algorithm where before going down to a node, we split it if it is full. The advantage of splitting before is, we never traverse a node twice. If we don’t split a node before going down to it and split it only if a new key is inserted (reactive), we may end up traversing all nodes again from leaf to root. This happens in cases when all nodes on the path from the root to leaf are full. So when we come to the leaf node, we split it and move a key up. Moving a key up will cause a split in parent node (because the parent was already full). This cascading effect never happens in this proactive insertion algorithm. There is a disadvantage of this proactive insertion though, we may do unnecessary splits. 