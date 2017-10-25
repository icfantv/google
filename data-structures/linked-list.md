# Linked Lists
Source: [Wikipedia](https://en.wikipedia.org/wiki/Linked_list), et. al.

A linear collection of data elements in which linear order is not given by physical placement in memory.  Rather, each element points to the next via means of a reference.

It is a data structure consisting of a group of nodes which together represent a sequence:

`12 •--> 99 •--> 37 •--> ⊠`

For a doubly-linked list, an additional reference is added to each element that points to the previous element.

## Performance
| Operation| Average                | Worst Case                |
|----------|------------------------|---------------------------|
| Insert   | O(1) or constant time  | O(1) or constant time     |
| Read     | O(n) or linear time    | O(n) or linear time       |
| Update   | O(n) or linear time    | O(n) or linear time       |
| Delete   | O(n) or linear time    | O(n) or linear time       |

## Advantages
Source: [Wikipedia](https://en.wikipedia.org/wiki/Linked_list)

* Linked lists are a dynamic data structure, which can grow and be pruned, allocating and deallocating memory while the program is running.
* Insertion and deletion node operations are easily implemented in a linked list.
* Dynamic data structures such as stacks and queues can be implemented using a linked list.
* There is no need to define an initial size for a linked list.
* Items can be added or removed from the middle of list.
* Backtracking is possible in two way linked list.

## Disadvantages
Source: [Wikipedia](https://en.wikipedia.org/wiki/Linked_list)

* They use more memory than arrays because of the storage used by their pointers.
* Nodes in a linked list must be read in order from the beginning as linked lists are inherently sequential access.
* Nodes are stored incontiguously, greatly increasing the time required to access individual elements within the list, especially with a CPU cache.
* Difficulties arise in linked lists when it comes to reverse traversing. For instance, singly linked lists are cumbersome to navigate backwards and while doubly linked lists are somewhat easier to read, memory is consumed in allocating space for a back-pointer.

## Implementation
### Java
```java
import java.util.List;

public class LinkedListTest {

  public static void main(String[] args) {

    LinkedList ll = new LinkedList();
    final List<Integer> data = List.of(1, 2, 3);

    data.forEach(ll::add);
    assert ll.size() == 3;

    Node current = ll.head();
    for (int i = 1; i <= 3; i++) {
      assert current.getData() == i;
      current = current.getNext();
    }
  }

  static class Node {

    private int data;
    private Node next = null;

    Node(int value) {
      this.data = value;
    }

    public int getData() {
      return this.data;
    }

    public Node getNext() {
      return this.next;
    }

    public void setNext(final Node nextNode) {
      this.next = nextNode;
    }
  }

  static class LinkedList {

    private int size = 0;
    private Node head = null;
    private Node current = null;

    void add(int value) {

      final Node node = new Node(value);
      if (head == null) {
        this.head = node;
      } else {

        while (this.current.next != null) {
          this.current = this.current.next;
        }

        this.current.next = node;
      }

      this.current = node;
      this.size++;
    }

    int size() {
      return this.size;
    }

    Node head() {
      return this.head;
    }
  }
}
```
### Javascript
