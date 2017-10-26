# Merge Sort
Source: [Wikipedia](https://en.wikipedia.org/wiki/Merge_sort)

A general purpose, comparison based sorting algorithm that utilizes a divide and conquer method of breaking down a list into smaller and smaller lists until _n_ lists of size one are had and then repeatedly merges adjacent lists until one list remains.

Conceptually, the algorithm works like this:

![merge sort](https://upload.wikimedia.org/wikipedia/commons/c/cc/Merge-sort-example-300px.gif)

## Performance
| Performance Type | Performance                    |
|:-----------------|:-------------------------------|
| Best case        | O(_n log n_) or O(_n_)         |
| Worst case       | O(_n log n_)                   |
| Average          | O(_n log n_)                   |
| Worst case space | O(_n_) total, O(_n_) auxiliary |

## Algorithm

### TypeScript
```typescript

export class Mergesort {

  public static sort(list: number[] = []): number[] {

    if (list.length <= 1) {
      return list;
    }

    let left: number[] = [];
    let right: number[] = [];
    list.forEach((item: number, index: number) => {
      if (index < (list.length / 2)) {
        left.push(item);
      } else {
        right.push(item);
      }
    });

    left = Mergesort.sort(left);
    right = Mergesort.sort(right);

    return Mergesort.merge(left, right);
  }

  private static merge(left: number[] = [], right: number[] = []): number[] {

    const result: number[] = [];
    while (left.length && right.length) {
      if (left[0] <= right[0]) {
        result.push(left.pop());
      } else {
        result.push(right.pop());
      }
    }

    // either left or right may still have elements, so consume them
    left.forEach((item: number) => result.push(item));
    right.forEach((item: number) => result.push(item));

    return result;
  }
}

```