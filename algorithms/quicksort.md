# Quick Sort
Source: [Wikipedia](https://en.wikipedia.org/wiki/Quicksort)

A general purpose, comparison based sorting algorithm that utilizes a divide and conquer method of picking a pivot point in a list, moving all items less than the pivot to be before and greater than the pivot to be after.  When this is done, the pivot is in its final position.  This process is repeated recursively with the smaller values and the larger ones.

Conceptually, the algorithm works like this:

![quick sort](https://upload.wikimedia.org/wikipedia/commons/6/6a/Sorting_quicksort_anim.gif)

## Performance
| Performance Type | Performance            |
|:-----------------|:-----------------------|
| Best case        | O(_n log n_) or O(_n_) |
| Worst case       | O(_n^2_) (rare)        |
| Average          | O(_n log n_)           |
| Worst case space | O(_n_) or O(_log n_)   |

## Algorithm

### TypeScript
```typescript

export class Quicksort {

  public static sort(list: number[] = [], low: number = 0, high: number = list.length - 1): void {

    if (low < high) {
      const p: number = Quicksort.partition(list, low, high);
      Quicksort.sort(list, low, p - 1);
      Quicksort.sort(list, p + 1, high);
    }
  }

  private static partition(list: number[] = [], low: number, high: number): number {

    const pivot: number = list[high];
    let i: number = low - 1;
    for (let j = low; j < high - 1; j++) {
      if (list[j] < pivot) {
        i++;
        const temp: number = list[i];
        list[i] = list[j];
        list[j] = temp;
      }
    }

    if (list[high] < list[i + 1]) {
      const temp: number = list[i + 1];
      list[i + 1] = list[high];
      list[high] = temp;
    }

    return i + 1;
  }
}

```