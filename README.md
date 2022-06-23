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
* It is mostly used for implementing Stacks and Queues.
* 
