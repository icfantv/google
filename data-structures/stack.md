# Stacks
Source: [Wikipedia](https://en.wikipedia.org/wiki/Stack_(abstract_data_type))

A stack is a collection in which elements are arranged in insertion order and has two primary operations `push` and `pop`.  The `push` operation places a new element into the stack and the `pop` operation removes the most recently inserted element.  A `peek` operation may also exist which allows visiblity into the top-most element in the stack but without removing the element.

The order the elements come out of the stack give rise to its alternative name, LIFO (last-in first-out).

### Implementation
#### Javascript
```
const stack = [];
stack.push(2);       // stack is now [2]
stack.push(5);       // stack is now [2, 5]
const i = stack.pop(); // stack is now [2], i === 5
```
