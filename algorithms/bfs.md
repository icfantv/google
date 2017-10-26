# Breadth First Search
Source [Wikipedia](https://en.wikipedia.org/wiki/Breadth-first_search)

An algorithm for traversing tree or graph structures by starting at the root node and exploring neighboring nodes first before moving to the next level neighbors.

This example shows the order of node traversal:

![breadth first tree](https://upload.wikimedia.org/wikipedia/commons/3/33/Breadth-first-tree.svg)

## Performance
| Operation | Average          |
|:----------|:-----------------|
| Search    | O(\|V\| + \|E\|) |

## Iterative Algorithm

```typescript
export interface INode {
  value: any;
  children: INode[];
}

export class BreadthFirstSearch {

  private root: INode;

  constructor() {
    // generate tree
  }

  public bfs(value: any): INode {
    return BreadthFirstSearch.findValue(value, this.root);
  }

  private static findValue(value: any, node: INode): INode {

    let result: INode = null;
    if (node.value === value) {
      result = node;
    } else {

      let doContinue = true;
      const queue: INode[] = [node];
      while (queue.length && doContinue) {
        const currentNode: INode = queue.shift(); // caution, this is O(n), where n is # of elements in array
        for (const child: INode in currentNode.children) {

          if (child.value === value) {
            doContinue = false;
            result = child;
            break;
          } else {
            queue.push(child);
          }
        }
      }
    }

    return result;
  }
}

```
