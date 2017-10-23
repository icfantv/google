# What to Know
Not inclusive, just a "must know" list.  For each topic, understand how to implement and use them.  And where applicable, the space and time complexity.

Practice implementing the data structures and algorithms.  Might be asked to implement them in your interview or a modification of them.  Either way, the more comfortable you are with them, the better.

## Advice for Technical Questions
A technical interview question can be solved utilizing a five step approach:

1. Ask your interviewer questions to resolve ambiguity.
2. Design an Algorithm
3. Write pseudo-code first, but make sure to tell your interviewer that you’re writing pseudo-code! Otherwise, he/she may think that you’re never planning to write “real” code, and many interviewers will hold that against you.
4. Write your code, not too slow and not too fast.
5. Test your code and carefully fix any mistakes.

### Ask Questions
Ask questions to resolve ambiguities or uncertainties.  Confirm inputs meet (or don't meet) certain criteria.  Also confirm outputs and assumptions made (as applicable).  **Derive tests from the inputs/outputs.**

* What are the data types?
* How much data is there?
* Use of third party libs?
	* Say, for parallellism
* Who is the user?  (if relevant)

### Design an Algorithm
This is probably going to be the tough part.  Follow the steps [outlined here](#algorithm-approaches) for help.  Don't forget to think about:

* What are the space and time complexities?* What happens if there is a lot of data?* Does your design cause other issues? (e.g. if you modify an existing, well-known algorithm, did you change the big-O time for operations?)* If there are other issues, did you make the right trade-offs?* Have you leveraged any specific information given to you?  (**Pay attention to this!**  Google interviewers will specifically look for whether or not you listen to and utilize any advice/tips/etc...)
 * This includes, e.g., data types for inputs **AND** during your actual white-boarding session.

### Pseudo-Code
Use pseudo-code to help outline thoughts clearly and to initially hand-wave over details.  Just make sure you tell the interviewer you're writing pseudo-code.

### Code
Don't rush through coding!  Be slow but methodical.
* Use data structures generously - create objects as applicable.  Show you care about good OOD.
* Don't crowd your coding

### Test
Test your code!
* Extreme cases:  0, negative, `null`, maximums, etc...
* User error:  what if user passes in `null` or negative values?
* General case:  test the normal use case

If the algorithm is complicated or highly numerical (bit shifting, arithmetic, etc...), consider testing while writing code rather than just at the end.

When you find mistakes, DEBUG YOUR CODE!  Don't just "randomly" change stuff to fix the error.  Think about WHY the bug is occurring.  If you just start changing stuff without thinking about it, it's going to be a HUGE red flag in your interview and as well it should.

# Data Structures
This section contains a list of the MINIMAL amount of data structures you should know for the interview:

* [Hash Tables](data-structures/hash-table.md)
* [Linked Lists](data-structures/linked-list.md)
* [Lists](data-structures/list.md)
* [Queues](data-structures/queue.md)
* [Stacks](data-structures/stack.md)
* [Trees](data-structures/tree.md)
* [Tries](data-structures/trie.md)


# Algorithm Approaches
There is no magic panacea for determining an algorithm.  In fact, most problems have more than one solution.  Note that they can also be mix-and-matched.

TBH, I started filling this in, but it was essentially the same information in _Cracking the Coding Interview_ so for all the juicy details, just read that (which you should do anyway).

# Algorithms
[This section](algorithms.md) contains a list of the MINIMAL amount of algorithms you should know for the interview.

# Concepts
[This section](concepts.md) contains a list of the MINIMAL amount of concepts you should know for the interview.
