# Hash Tables
Source: [Wikipedia](https://en.wikipedia.org/wiki/Hash_table), et. al.

A data structure that maps keys to values using a hash function to computer an _index_ into an array of buckets or slots from which the desired value can be found.

Ideally, the hash function will assign each key to a unique bucket, but most hash table designs employ an imperfect hash function, which might cause hash collisions where the hash function generates the same index for more than one key. Such collisions must be accommodated in some way.

E.g.,
```json
{
  key: value,
  another_key: another_value
}
```
![hash table](https://upload.wikimedia.org/wikipedia/commons/7/7d/Hash_table_3_1_1_0_1_0_0_SP.svg)


Some computer science problems can be solved faster by transforming array-based data into a hash table first, an O(n) operation, so that subsequent reads are only O(1).

## Performance
| Operation| Average | Worst Case |
|----------|---------|------------|
| Insert   | O(1)    | O(n)       |
| Read     | O(1)    | O(n)       |
| Update   | O(1)    | O(n)       |
| Delete   | O(1)    | O(n)       |
