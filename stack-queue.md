![](https://miro.medium.com/max/1000/0*-y92CX3NIm9SkYSx.png)

# Stacks and Queues

### Stacks
* A stack consists of nodes that reference the next node in the stack but not the previous
* Nodes put on the stack are pushed, and nodes taken off the stack are popped
* When you peek, you see the top value of the stack
* `IsEmpty` will return `true` if the stack is empty
* Stacks are First In Last Out (FILO)/Last In First Out (LIFO)
* The topmost item is called the `top`, and when you pop the top, you set the next top as top.next
* When you push a new top (O(1)) you set the new node as the new top, and it's next as the old top
* To pop, check if the stack is empty.
* Then make a reference to the same node that `top` points to
* Then reassign top to next.
* To peek, return top.value
* If top is NULL, isEmpty is true


![](https://cdn.programiz.com/sites/tutorial2program/files/stack-operations.png)
s
##### What is Stack? FILO/LIFO

- A stack is.... a *stack*!
  - An *idea*, not an *implementation*
- **F**irst **I**n **L**ast **O**ut / **L**ast **I**n **F**irst **O**ut
- pop() and push()
  - O(1)
  - push onto and pop off of the stack
- peek()   
  - O(1)
  - inspect the top most thing in the stack
  - with a vanilla stack, you don't know the height of the stack and what is below
- isEmpty()  
  - O(1)
- **These are the only things you can do to a stack, even if it's in array form (for ex)**
  - Huge value in keeping it as a 'stack' 


### Queue
* Enqueue - nodes that are added to the queue
* Dequeue - nodes that are removed from the queue
* Front is the first node of the queue
* Rear is the last node of the queue
* Peek to view the front node in the queue
* isEmpty is true when the queue is empty
* Queues are FIFO
* Enqueue by adding to the end of the queue - change rear.next to be the new node, and make the new node the rear
* Check isEmpty before dequeueing
* Dequeueing is similar to taking a node off a stack
* Return the value after dequeueing


![](https://miro.medium.com/max/1236/1*6Mq-ogES1TuIFxlC7bMcXw.png)

##### What is Queue? FIFO/LILO

- Instead of top and bottom, there's a notion of front and back
  - *enqueue*: adds to front of queue
  - *dequeue*: takes off back of queue
  - can also *peek* and check *isEmpty*