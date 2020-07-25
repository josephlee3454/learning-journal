# Binary Trees
* Trees can have any number of children per node, but Binary Trees restrict the number of children to two (hence our left and right children).

# Binary search trees
* Searching a BST can be done quickly, because all you do is compare the node you are searching for against the root of the tree or sub-tree. If the value is smaller, you only traverse the left side. If the value is larger, you only traverse the right side.

# Terms:
* Node: the individual item thet  makes up a data structure
* Root : the first top node in the tree
* laft-child: the node that is positioned to the left of aroot or node 
* Right-child: the node to the right of a root or node 
* Edge: The edge in a tree is the link between a parent and child node
* Leaf: A leaf is a node that does not contain any children
* Height: The height of a tree is determined by the number of edges from the root to the bottommost node

# Traversals 
* An important aspect of trees is how to traverse them. Traversing a tree allows us to search for a node, print out the contents of a tree, and much more!
### two catorgories of traversals when it comes to trees:
* Depth first: Depth first traversal is where we prioritize going through the depth (height) of the tree first. There are multiple ways to carry out depth first traversal, and each method changes the order in which we search/print the root. Here are three methods for depth first traversal: 
* Pre-order: root >> left >> right
* In-order: left >> root >> right
* Post-order: left >> right >> root
* the most common wat to to traverse a tree is to use recursion.
# pre-order 
* Pre-order means that the root has to be looked at first. In our case, looking at the root just means that we output its value. When we call preOrder for the first time, the root will be added to the call stack: