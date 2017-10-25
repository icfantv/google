# Binary Trees
Source: [Wikipedia](https://en.wikipedia.org/wiki/Binary_tree)

A tree data structure in which each node has at most two children, referred to as the _left_ and _right child_.

Example:

![tree](https://upload.wikimedia.org/wikipedia/commons/f/f7/Binary_tree.svg)

# Binary Search Trees (BST)
Source: [Wikipedia](https://en.wikipedia.org/wiki/Binary_search_tree)

A special type of binary tree such that the nodes are sorted by their key:

![bst](https://upload.wikimedia.org/wikipedia/commons/d/da/Binary_search_tree.svg)

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
![unbalanced binary tree](https://upload.wikimedia.org/wikipedia/commons/a/a9/Unbalanced_binary_tree.svg)

The same tree, but after balancing:
![balanced binary tree](https://upload.wikimedia.org/wikipedia/commons/0/06/AVLtreef.svg)

## Balanced BST Performance
| Operation | Average    | Worst Case |
|:----------|:-----------|:-----------|
| Insert    | O(_log n_) | O(_log n_) |
| Read      | O(_log n_) | O(_log n_) |
| Update    | O(_log n_) | O(_log n_) |
| Delete    | O(_log n_) | O(_log n_) |
