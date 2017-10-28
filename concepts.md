# Big-O Time

A term in computer science used to describe the performance or complexity of an algorithm.  Specifically, it describes the worst-case scenario and is typically used to indicate the time an algorithm will take to execute.

# Bit Manipulation

## Bitwise addition

Things to note:

* `0 + 0 = 0`
* `0 + 1 = 1`
* `1 + 1 = 0` with a carry bit
* `carry bit + 1 + 1 = 1` with another carry bit

### Bitwise Addition Example

```
  ***
   0111
 + 1110
 ------
  10101

* - denotes carry bit
```

## Bitwise subtraction

The complement method (below) of bitwise subtraction flips the problem to a bitwise addition and discards the extra bit.

### Bitwise Subtraction Example

```
Step:          1             2          3           4         5
----------------------------------------------------------------------------

  101         101                      100         101
-  11  -->  - 011  -->  011 --> 100  +   1  -->  + 101
-----       -----                    -----       -----
                                       101        1010  -->  010, or just 10
```

1. We set up the basic bitwise subtraction problem and add any leading zeros, if necessary.
2. Take the one's complement of the lower number, that is, flipping the bits.
3. Add one to this new number.
4. Solve the problem using normal, bitwise addition rules.
5. Drop the leading 1 as this is the overflow bit.  If there wasn't an overflow bit, then we tried to subtract a larger number from a smaller one.

## Operations Table

| Operation |              |              |              |              |
|:----------|:-------------|:-------------|:-------------|:-------------|
| And (&)   | `0 & 0 = 0`  | `1 & 0 = 0`  | `0 & 1 = 0`  | `1 & 1 = 1`  |
| Or (\|)   | `0 | 0 = 0`  | `1 | 0 = 1`  | `0 | 1 = 1`  | `1 | 1 = 1`  |
| Xor (^)   | `0 ^ 0 = 0`  | `1 ^ 0 = 1`  | `0 ^ 1 = 1`  | `1 ^ 1 = 0`  |



# Factory Design Pattern

# Memory (Stack vs. Heap)

# Recursion

# Singleton Design Pattern

# Tree Traversal