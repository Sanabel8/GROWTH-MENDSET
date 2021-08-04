Stacks and Queues
* What is a Stack : A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.
* terminology for a stack is :
1. Push 
2. Pop 
3. Top
4. peek
5. IsEmpty

* Stacks follow these concepts:
- FILO  First In Last Out
- LIFO  Last In First Out
- Stack Visualization 
* When you push something to the stack, it becomes the new top
* When you pop something from the stack, you pop the current top
* set the next top as top.next
- Push O(1) 
* Pushing a Node onto a stack will always be an O(1) operation
* no matter how many Nodes (n) you have in the stack.

* steps for pushing node :
1. First, you should have the Node that you want to add.
2.  you need to assign the next property of Node 5 to reference the same Node that top is referencing: Node 4
3. re-assign our reference top to the newly added Node, Node 5.
```ALOGORITHM push(value)
// INPUT <-- value to add, wrapped in Node internally
// OUTPUT <-- none
   node = new Node(value)
   node.next <-- Top
   top <-- Node
```
- Pop O(1)
* Popping a Node off a stack is the action of removing a Node from the top

* steps for pop the top node :
1. create a reference named temp that points to the same Node that top points to.
2. re-assign top to the value that the next property is referencing.
3. re-assign top to be Node 4
4. remove Node 5 safely
5. we return the value of the temp Node that was just popped off.

```ALGORITHM pop()
// INPUT <-- No input
// OUTPUT <-- value of top Node in stack
// EXCEPTION if stack is empty

   Node temp <-- top
   top <-- top.next
   temp.next <-- null
   return temp.value
```
- Peek O(1)
- IsEmpty O(1)

* What is a Queue
* terminology for a queue is:
1. Enqueue
2. Dequeue
3. Front
4. Rear
5. Peek
6. IsEmpty


































