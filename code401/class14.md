# Trees
Binary Trees, Binary Search Trees, and K-ary Trees.

## Common Terminology
1. Node :  A Tree node is a component which may contain it’s own values, and references to other nodes
2. ROOT : node at the beginning of the tree
3. K :  the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2
4. Left : A reference to one child node, in a binary tree
5. Right : A reference to the other child node, in a binary tree
6. Edge : is the link between a parent and child node
7. Leaf : node that does not have any children
8. Height:  the number of edges from the root to the furthest leaf

# Traversals
* type of traversals:
1. Depth First : where we prioritize going through the depth (height) of the tree first
2. Breadth First : Breadth first traversal iterates through the tree by going through each level of the tree node-by-node.
## Depth First
* methods for depth first traversal:
. Pre-order: root >> left >> right
. In-order: left >> root >> right
. Post-order: left >> right >> root
* recursion: The most common way to traverse through a tree
* pseudocode for pre-order traversal :
* ALGORITHM preOrder(root)
```
  OUTPUT <-- root.value

  if root.left is not NULL
      preOrder(root.left)

  if root.right is not NULL
      preOrder(root.right)
```
* ALGORITHM inOrder(root)
```

    if root.left is not NULL
        inOrder(root.left)

    OUTPUT <-- root.value

    if root.right is not NULL
        inOrder(root.right)
```
* ALGORITHM postOrder(root)
```  if root.left is not NULL
        postOrder(root.left)

    if root.right is not NULL
        postOrder(root.right)

    OUTPUT <-- root.value
```
* When we call preOrder for the first time, the root will be added to the call stack
* we start reading our preOrder function’s code from top to bottom.
*  the heart of recursion: when we complete a function call, we pop it off the stack and are able to continue execution through the previous function call
* The biggest difference between each of the traversals is when you are looking at the root node.
## Breadth First
*  breadth first traversal uses a queue to traverse the width/breadth of the tree. Let’s break down the process.
* Pseudocode
```  Queue breadth <-- new Queue()
  breadth.enqueue(root)

  while breadth.peek()
    node front = breadth.dequeue()
    OUTPUT <-- front.value

    if front.left is not NULL
      breadth.enqueue(front.left)

    if front.right is not NULL
      breadth.enqueue(front.right)
```
## Binary Tree Vs K-ary Trees
* Binary Trees restrict the number of children to two (hence our left and right children).
* There is no specific sorting order for a binary tree. 
* K-ary Tree : If Nodes are able have more than 2 child nodes.
* K to refer to the maximum number of children that each Node is able to have.
* With every Node we dequeue, we check it’s list of childre and enqueue each one
* Pseudocode ALGORITHM breadthFirst(root)
```
  Queue breadth <-- new Queue()
  breadth.enqueue(root)

  while breadth.peek()
    node front = breadth.dequeue()
    OUTPUT <-- front.value

    for child in front.children
        breadth.enqueue(child)
```
## Adding a node
* in a binary tree, it really doesn’t matter where a new node gets placed.
* The Big O time complexity for inserting a new node is O(n)
* Searching for a specific node will also be O(n)
* The Big O space complexity for a node insertion using breadth first insertion will be O(w)
* The maximum width for a perfect binary tree, is 2^(h-1)
## Binary Search Trees (BST)
* is a type of tree that does have some structure attached to it
* where all values that are smaller than the root are placed to the left, and all values that are larger than the root are placed to the right.
* The best way to approach a BST search is with a while loop
* The Big O time complexity of a Binary Search Tree’s insertion and search operations is O(h)
* The Big O space complexity of a BST search would be O(1)
* A function fun is called direct recursive if it calls the same function fun. 
* A function fun is called indirect recursive if it calls another function say fun_new and fun_new calls fun directly or indirectly. 

























 