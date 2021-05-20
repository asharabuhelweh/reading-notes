# Linked Lists

A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.

Types of Linked List
Following are the various types of linked list.

1. Simple Linked List − Item navigation is forward only.

2. Doubly Linked List − Items can be navigated forward and backward.

3. Circular Linked List − Last item contains link of the first element as next and the first element has a link to the last element as previous.

![compare linked lists and arrays](https://miro.medium.com/max/615/1*iMYmkYDCSrXXdwpbqm-ekA.jpeg)

Linked lists are mainly a linear data structure that consists of arranged nodes. Each node contains a specific type of data and a reference to the next node in the list, which, as well, contain data and a reference to the next. Having this reference element allows each node to live wherever a place is available in the memory. Linked lists, as a result, don't have to allocate blocks of memory before runtime. They instead allocate only memory needed for the data they contain whenever needed by the user or the program during the runtime.

![img](https://miro.medium.com/max/2416/0*4Id-3IMNQHihLJAg.png)


![linked lists performance](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/images/LinkedList4.PNG)

**what is Big O?**

 Big O Notation is a way of evaluating the performance of an algorithm.

 As far as linked lists go, however, the two types of Big O equations to remember are O(1) and O(n).

 * An O(1) function takes constant time, which is to say that it doesn’t matter how many elements we have, or how huge our input is: it’ll always take the same amount of time and memory to run our algorithm.
 
  * An O(n) function is linear, which means that as our input grows (from ten numbers, to ten thousand, to ten million), the space and time that we need to run that algorithm grows linearly.