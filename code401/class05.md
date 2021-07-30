Linked Lists
* Linked List : 1. sequence of Nodes each Node references the next Node in the link.
                42. A data structure that contains nodes that links/points to the next node in the list.
* type of linked list : Singly and Doubly.
* Singly :there is only one reference, and the reference points to the Next node in a linked list.
* Nodes :are links that live in a linked list
* Each node contains the data for each link.
* Next :Next. This property contains the reference to the next node.
* Head is a reference of type Node to the first node in a linked list,is always the first node in a Linked List).
* Current is a reference of type Node
* you create a new Current variable at the Head to guarantee you are starting from the beginning of the linked list.
* The Next property is exceptionally important because it will lead us where the next node is and allow us to extract the data appropriately.
* The best way to approach a traversal is through the use of a while() loop.
* If we accidentally end up trying to traverse on a node that is null, a NullReferenceException gets thrown and our program will crash/end.

Traversal Big O
* The Big O of (time) for Includes would be O(n). => n represents the number of nodes in the linked list.
* The Big O of space for Includes would be O(1).

Adding a Node
* Adding O(1)
* If we want to add a node with an O(1),we have to replace the current Head of the linked list with the new node.
* we make anew node and have value passed on Add() method 
* and next set as null
* we will be assigning it to the same allocation in memory as the node it is pointing too. In this case, it’s Node1

Add Big O
*  the number of Nodes linked list always O(1) time and space  

Adding a Node O(n)
* create a new node (node6).
* The Next will be null 
* start adding by AddBefore or AddAfter methods 
* AddBefore method that we will demonstrate where will insert the new node passed on the value
 
AddBefore Big O
* The time efficiency of this transaction would be O(n) 
* Space efficiency would stay at an O(1) 

Prerequisites
* When making your Node class, consider requiring a value to be passed in to require that each node has a value.

What’s a Linked List, Anyway?
* data structures, which are the different ways that we can organize our data; variables, arrays, hashes, and objects are all types of data structures. 

Linear data structures
* One characteristic of linked lists is that they are linear data structures
* in order to get to the end of the list, we have to go through all of the items in the list in order, or sequentially.
* When we organize our data into hashes (sometimes called dictionaries), we’re implementing a non-linear data structure.
*  when we use arrays in our code, we’re implementing a linear data structure! It can be helpful to think of arrays and linked lists as being similar in the way that we sequence data
* The biggest differentiator between arrays and linked lists is the way that they use memory in our machines.
* when a linked list is born, it doesn’t need 7 bytes of memory all in one place. One byte could live somewhere, while the next byte could be stored in another place in memory altogether
* arrays are static data structures
* linked lists are dynamic data structures.
* A node only knows about what data it contains, and who its neighbor is.


*  Big O Notation is a way of evaluating the performance of an algorithm.
*  That’s exactly what Big O Notation takes into account: the speed and efficiency 
* An O(1) function takes constant time, 
* An O(n) function is linear, which means that as our input grows 
* O(n²) clearly takes exponentially more time and memory the more elements that you have
* all we need to do in order to add something to our linked list is figure out which pointer needs to point to where.
* insert node at the very beginning:
1. First, we find the head node of the linked list.
2. make our new node, and set its pointer to the current first node of the list
3. we rearrange our head node’s pointer to point at our new node.
** has a space time complexity that is constant, or O(1).

* the rule of linked list :a linked list is usually efficient when it comes to adding and removing most elements, but can be very slow to search and find a single element






























