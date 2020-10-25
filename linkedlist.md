![](https://hackernoon.com/hn-images/1*GOKmkucFHN_gmTMUtyC2sQ.png)
# Linked List

**What is a Linked List?**

A linked list is a linear data structure similar to an array. However, unlike arrays, elements are not stored in a particular memory location or index. Rather each element is a separate object that contains a pointer or a link to the next object in that list.

![](https://res.cloudinary.com/practicaldev/image/fetch/s--YbkBeKgv--/c_imagga_scale,f_auto,fl_progressive,h_500,q_auto,w_1000/https://cl.ly/8a0b74c08365/Image%25202018-09-13%2520at%252011.17.28%2520AM.png)

**In JavaScript, a linked list looks like this:**

```
const list = {
    head: {
        value: 6
        next: {
            value: 10                                             
            next: {
                value: 12
                next: {
                    value: 3
                    next: null	
                    }
                }
            }
        }
    }
};
```

* An advantage of Linked Lists

Nodes can easily be removed or added from a linked list without reorganizing the entire data structure. This is one advantage it has over arrays.

* Disadvantages of Linked Lists

   - Search operations are slow in linked lists. Unlike arrays, random access of data elements is not allowed. Nodes are accessed sequentially starting from the first node.
   - It uses more memory than arrays because of the storage of the pointers.


![](https://miro.medium.com/max/2638/1*typvDGtljh_06e3Da7ciLw.png)
### Types of Linked Lists
1. **Singly Linked Lists:** Each node contains only one pointer to the next node. This is what we have been talking about so far.
2. **Doubly Linked Lists:** Each node contains two pointers, a pointer to the next node and a pointer to the previous node.
3. **Circular Linked Lists:** Circular linked lists are a variation of a linked list in which the last node points to the first node or any other node before it, thereby forming a loop.


### linked list properties:
* Successive nodes are connected by pointers.
* The last node points to null.
* A head pointer is maintained which points to the first node of the list.
* A linked list can grow and shrink in size during execution of the program.
* It can be made just as long as required.
* It allocates memory as the list grows. Unlike arrays, which have a fixed size. Therefore, the upper limit on the number of elements must be known in advance. Generally, the allocated memory is equal to the upper limit irrespective of the usage. This is one the key advantages of using a linked list over an array.



##### Find
It’s very simple, we just need to store the current item and use a for or while loop to use our pointers to update current until we’re at the item we want.

![](https://assets.digitalocean.com/articles/alligator/js/linked-lists-implementation/linked-list-find.gif)

Of course, this gives us an O(n) search time, but since we’re using a doubly linked list we can just start from the tail if what we want is past the middle of the list, giving us O(n / 2).

```
find(index) {
  let current
  if (index < 0 || index >= this.length) return undefined;

  if (index <= this.length / 2) {
    current = this.head;
    for (let i = 0; i < index; i++) current = current.next;
  } else {
    current = this.tail;
    for (let i = this.length; i > index; i--) current = current.prev;
  }

  return current;
}
```

##### Insert and Remove
Now that we have our little utility in place we can use it to find the item in the index we want then set the pointers on it and the item before and after it to our new node, thus “stitching” it into place.

![](https://assets.digitalocean.com/articles/alligator/js/linked-lists-implementation/linked-list-insert.gif)

```
insert(val, index) {
  if (index < 0 || index > this.length) return null;
  if (index === this.length) return this.addTail(val);
  if (index === 0) return this.addHead(val);

  let prev = this.find(index - 1),
      newNode = new Node(val),
      temp = prev.next;

  prev.next = newNode;
  newNode.next = temp;
  newNode.prev = prev;

  this.length++;
  return true;
}
```


There is a table below which displays a big O notation of each method described in the article. If you haven't ever heard about big O.

| Method                                                        |  Method |
|---------------------------------------------------------------|---------|
| addToTheEnd(value)                                            | n       |
| insertInPosition(value, position) at the end or beginning*  | n or 1  |
| getNodeByPosition(position)                                   | n       |
| removeFromPosition(position) from the end or beginning*     | n or 1  |
| getIndexOf(value)                                             | n       |
| removeElementByValue(value)                                   | n       |
| getLength()                                                   | 1       |
| isEmpty()                                                     | 1       |
| print()                                                       | n       |

* — beginning means position = 0.
