# Queues
Source: [Wikipedia](https://en.wikipedia.org/wiki/Queue_(abstract_data_type))

A Queue is a collection in which the entities are kept in order and the principal (or only) operations on the collection are the addition of entities to the rear terminal position, known as enqueue, and removal of entities from the front terminal position, known as dequeue.
This makes the queue a FIFO (first-in first-out) data structure, that is, they are removed in insertion order - elements inserted first are removed first.
Often a _peek_ or _front_ method exists to allow visibility into the first item without dequeuing it.

### Implementation
#### Javascript
```
const queue = [];
queue.push(2);         // queue is now [2]
queue.push(5);         // queue is now [2, 5]
let i = queue.shift(); // queue is now [5], i === 2
```

**NB**:  [The ECMAScript Language Specification](https://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.9) indicates that `Array.shift()` is an O(n) operation.  A better implementation of a queue in Javascript would be
[this version](http://code.stephenmorley.org/javascript/queues) which maintains an internal offset (pointer) to the head of the queue and calls `Array.slice` to remove the empty cells from the head of the queue:

```
  const queue = [];
  let offset = 0;

  this.dequeue = function() {

    // if the queue is empty, return immediately
    if (queue.length == 0) return undefined;

    // store the item at the front of the queue
    const item = queue[offset];

    // increment the offset and remove the free space if necessary
    if (++offset * 2 >= queue.length){
      queue = queue.slice(offset);
      offset = 0;
    }

    return item;
  }

```

## Priority Queue
Source: [Wikipedia](https://en.wikipedia.org/wiki/Priority_queue)

A queue whereby elements also have a "priority" associated with them.  On dequeuing, higher priority items are served before lower priority ones.  If two elements have the same priority, they are served in insertion order.

## Heap
Source: [Wikipedia](https://en.wikipedia.org/wiki/Heap_(data_structure))

A specialized, tree-based structure that satisfies the _heap property_: if P is a parent node of C, then the _key_ (the _value_) of P is either greater than or equal to (_max heap_) or less than or equal to (_min heap_) the key of C.  The node at the "top" of the heap (with no parents) is called the _root_ node.

A binary heap:
```
             100
            /   \
           /     \
         19       36
        /  \     /  \
      17    3   25   1
     /  \
    2    7
```