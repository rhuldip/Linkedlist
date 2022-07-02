# LinkedList
## Pros
* Dynamic size based on future operations - add or remove
* Insertion or deletion in middle is easy as compared to Arrays
## Cons
* Take extra space for maintaining references to next object
* Does not support constant time retrieval like Arrays
* Spacial locality in memory not supported as elements in arrays are in different location in memory so retrieving of each elements take time whereas in Arrays its super fast 
## Types of LinkedList
### Singly LinkedList
```java
class Node {
  int data;
  Node next;
}
```
The first node is called as the head of the LinkedList. We always keep it safe with a variable like this - 
```java
Node head = new Node(1, null);
```
#### Applications
* It is mostly used for implementing Stacks and Queues
* To prevent the collision between the data in the hash map, we use a singly linked list

### Circular LinkedList
The last node points to the first node making a circle
#### Applications
* Round Robin scheduling technique in games/ applications
* Circular Escalators

### Doubly LinkedList
```java
class Node {
  int data;
  Node prev, next;
}
```
Each node has two pointers, one points to previous node and other to the next node
#### Applications
* Photo Gallery where after the end of photo gallery we can go back only
* Brower back and next button navigation

### Circular Doubly LinkedList
Doubly LinkedList where the head prev points to the tail and the tail next points to the head
#### Applications
* Implementation of advanced data structures like Fibonacci Heap
* Music Player
* Photo Gallery
### Unrolled LinkedList
```java
class UnrolledNode{
  int[] arr;
  int noOfElements;
  UnrolledNode next;
}
```
Unrolled LinkedList is a variation of LinkedList where multiple elements are kept inside a Node.
An array is maintained which keeps data. Usually the size of array is kept in such a way that the entire node fills a single cache line.
### Pros-
Since elements the stored in an array and since the array boost cache performance because of spatial locality, the search is faster.
Less overload because less number of next pointer are created.
Performance for operation(Insertion and Deletion) is better since we can easy find the position where we need to insert or delete by skipping the entire node based on noOfElements in that node.


References -
https://en.wikipedia.org/wiki/Unrolled_linked_list
https://brilliant.org/wiki/unrolled-linked-list/
https://www.geeksforgeeks.org/difference-between-spatial-locality-and-temporal-locality/

