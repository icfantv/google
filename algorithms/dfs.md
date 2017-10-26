# Depth First Search
Source: [Wikipedia](https://en.wikipedia.org/wiki/Depth-first_search)

An algorithm for traversing tree or graph structures by starting at the root node and exploring as far along each branch before back tracking.

This example shows the order of node traversal:

![depth first tree](https://upload.wikimedia.org/wikipedia/commons/1/1f/Depth-first-tree.svg)

## Performance
| Operation | Average          |
|:----------|:-----------------|
| Search    | O(\|V\| + \|E\|) |

## Recursive Algorithm

### TypeScript

```typescript
export interface INode {
  value: any;
  children: INode[];
}

export class DepthFirstSearch {

  private root: INode;

  constructor() {
    // generate tree
  }

  public dfs(value: any): INode {
    return this.findValue(value, this.root);
  }

  private findValue(value: any, node: INode): INode {

    let result: INode = null;
    if (node.value === value) {
      result = node;
    } else if (node.children && node.children.length) {

      for (const child of node.children) {
        result = this.findValue(value, child);
        if (result) {
          break;
        }
      }
    }

    return result;
  }
}
```

## Iterative Algorithm

```typescript
export interface INode {
  value: any;
  children: INode[];
}

export class DepthFirstSearch {

  private root: INode;

  constructor() {
    // generate tree
  }

  public dfs(value: any): INode {

    const stack: INode[] = [];
    let result: INode = null;
    stack.push(this.root);
    while (stack.length) {
      const node: INode = stack.pop();
      if (node.value === value) {
        result = node;
        break;
      } else {
        node.children.forEach((child: INode) => stack.push(child));
      }
    }

    return result;
  }
}
```