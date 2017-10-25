# Binary Trees
Source: [Wikipedia](https://en.wikipedia.org/wiki/Binary_tree)

A tree data structure in which each node has at most two children, referred to as the _left_ and _right child_.

Example:

```
       2
      / \
    /     \
   7       5
  / \       \
 2   6       9
    / \     /
   5  11   4
```

# Binary Search Trees (BST)
Source: [Wikipedia](https://en.wikipedia.org/wiki/Binary_search_tree)

A special type of binary tree such that the nodes are sorted by their key:

```
       8
      / \
    /     \
   3       10
  / \       \
 1   6       14
    / \     /
   4   7   13
```

## Performance
| Operation | Average    | Worst Case |
|:----------|:-----------|:-----------|
| Insert    | O(_log n_) | O(_n_)     |
| Read      | O(_log n_) | O(_n_)     |
| Update    | O(_log n_) | O(_n_)     |
| Delete    | O(_log n_) | O(_n_)     |

# Balanced BST
Source: [Wikipedia](https://en.wikipedia.org/wiki/Self-balancing_binary_search_tree)

A special type of BST that automatically keeps its height small for arbitrary insertions and deletions.

Unbalanced BST:
```
           50
          /  \
         /    \
       17      76
      /  \     /
     /    \   54
    9     23   \
     \    /    72
     14  19    /
     /        67
    12
```

The same tree, but after balancing:
```
           50
          /  \
         /    \
       17      72
      /  \     / \
     /    \   54  76
    12     23  \
   /  \    /   67
  9   14  19
```

## Balanced BST Performance
| Operation | Average    | Worst Case |
|:----------|:-----------|:-----------|
| Insert    | O(_log n_) | O(_log n_) |
| Read      | O(_log n_) | O(_log n_) |
| Update    | O(_log n_) | O(_log n_) |
| Delete    | O(_log n_) | O(_log n_) |
