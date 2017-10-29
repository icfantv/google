# Tree Traversal

## Pre-Order

![pre order](https://upload.wikimedia.org/wikipedia/commons/d/d4/Sorted_binary_tree_preorder.svg)

Pre-order: `F, B, A, D, C, E, G, I, H`

### Implementation

```javascript
function visit(node) {
  return node.value;
}

// Recursive
function recursivePreorder(node) {
  if (!node) {
    return;
  }

  visit(node);
  recursivePreorder(node.left);
  recursivePreorder(node.right);
}

// Iterative
function iterativePreorder(node) {

  if (!node) {
    return;
  }

  const s = [node];
  while (s.length) {

    node = s.pop();
    visit(node);

    // right child is pushed first so that left is processed first
    if (node.right !== null) {
      s.push(node.right);
    }
    if (node.left !== null) {
      s.push(node.left);
    }
  }
}
```

## In-Order

![in order](https://upload.wikimedia.org/wikipedia/commons/7/77/Sorted_binary_tree_inorder.svg)

In-order: `In-order: A, B, C, D, E, F, G, H, I`

### Implementation

```javascript
function visit(node) {
  return node.value;
}

// Recursive
function recursiveInOrder(node) {

  if (!node) {
    return;
  }

  recursiveInOrder(node.left);
  visit(node);
  recursiveInOrder(node.right);
}

// Iterative
function iterativeInOrder(node) {

  const s = [];
  while (s.length || node !== null) {

    if (node !== null) {
      s.push(node);
      node = node.left;
    }
    else {
      node = s.pop();
      visit(node);
      node = node.right;
    }
  }
}
```

## Post-Order

![post order](https://upload.wikimedia.org/wikipedia/commons/9/9d/Sorted_binary_tree_postorder.svg)

Post-Order:  `Post-order: A, C, E, D, B, H, I, G, F`

### Implementation

```javascript
function visit(node) {
  return node.value;
}

function recursivePostOrder(node) {

  if (!node) {
    return;
  }

  recursivePostOrder(node.left);
  recursivePostOrder(node.right);
  visit(node);
}
  // Iterative
  function iterativePostOrder(node) {

  const s = [];
  let lastNodeVisited = null;
  while (s.length || node !== null) {

    if (node !== null) {
      s.push(node);
      node = node.left;
    } else {

      const peekNode = s[0];

      // if right child exists and traversing node from left child, then move right
      if (peekNode.right !== null && lastNodeVisited !== peekNode.right) {
        node = peekNode.right;
      } else {
        visit(peekNode);
        lastNodeVisited = s.pop();
      }
    }
  }
}
```
