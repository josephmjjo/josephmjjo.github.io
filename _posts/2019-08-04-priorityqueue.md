---
title:  "What is Priority Queue?"
search: false
categories: 
  - DSandAL
---


Priority queue is an abstract data type which is like a regular queue or stack data structure, but where additionally each element has a "priority" associated with it.  

I think you should use "Heap" when you implement Priority Queue . because stack and queue have cons.
stack has disadvantages that all of the values have to move if you add or remove values
cons of the queue are you can't find immediately location what you wish to remove or add 
So usually, we should use "Binary Heap".   

Heap has two kind of sort way. max heap  and min heap. 
max heap must maximum value put the root of heap
min heap is reverse of max heap. minimum value must put at root 
In book, we write AdaptablePriorityQueue ADT to use PriorityQueue.

<!--stackedit_data:
eyJoaXN0b3J5IjpbNjg0OTg4NDU0LC0zNzA0Mjg2NjldfQ==
-->