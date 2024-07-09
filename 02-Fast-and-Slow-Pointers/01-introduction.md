## The Fast and Slow Pointers Pattern

The fast and slow pointers pattern uses two pointers to traverse an iterable data structure, but at different speeds, often to identify patterns, detect cycles, or find specific elements. The speeds of the two pointers can be adjusted according to the problem statement. Unlike the two pointers approach, which is concerned with data values, the fast and slow pointers approach is often used to determine specific patterns or structures in the data.

The key idea is that the pointers start at the same location and then start moving at different speeds. Generally, the slow pointer moves forward by a factor of one, and the fast pointer moves by a factor of two. This approach enables the algorithm to detect patterns or properties within the data structure, such as cycles or intersections. If there is a cycle, the two are bound to meet at some point during the traversal. To understand the concept, think of two runners on a track. While they start from the same point, they have different running speeds. If the track is circular, the faster runner will overtake the slower one after completing a lap.

### Examples

The following examples illustrate some problems that can be solved with this approach:

1. **Middle of the Linked List**: Given the head of a singly linked list, return the middle node of the linked list.

2. **Detect Cycle in an Array**: Given an array of non-negative integers where elements are indexes pointing to the next element, determine if there is a cycle in the array.

### Does Your Problem Match This Pattern?

Yes, if the following condition is fulfilled:

- **Linear Data Structure**: The input data can be traversed in a linear fashion, such as an array, linked list, or string.

In addition, if either of these conditions is fulfilled:

- **Cycle or Intersection Detection**: The problem involves detecting a loop within a linked list or an array or involves finding an intersection between two linked lists or arrays.
- **Find the Starting Element at the Second Quantile**: The problem involves finding the starting element of the second quantile, i.e., second half, second tertile, second quartile, etc. For example, the problem asks to find the middle element of an array or a linked list.

### Real-World Problems

Many problems in the real world use the fast and slow pointers pattern. Let’s look at some examples.

- **Symlink Verification**: A symbolic link, or symlink, is simply a shortcut to another file. Essentially, it’s a file that points to another file. Symlinks can easily create loops or cycles where shortcuts point to each other. To avoid such occurrences, a symlink verification utility can be used, and fast and slow pointers are useful in that case.

- **Compiling an Object-Oriented Program**: Compiling object-oriented programs often involves managing dependencies between various modules stored in separate files for easier maintenance. However, these dependencies can sometimes form cyclic relationships, leading to compilation errors. By employing the fast and slow pointers pattern, these cycles can be detected and resolved, ensuring smooth compilation and execution of the program.




## DSA Questions Solvable with Fast and Slow Pointers Pattern

1. **Middle of the Linked List**
   - Given the head of a singly linked list, return the middle node of the linked list.

2. **Detect Cycle in a Linked List**
   - Given the head of a linked list, determine if the linked list has a cycle in it.

3. **Cycle Length in a Linked List**
   - Given the head of a linked list that has a cycle, return the length of the cycle.

4. **Find the Start of the Cycle in a Linked List**
   - Given the head of a linked list that has a cycle, find the node where the cycle begins.

5. **Happy Number**
   - Determine if a number is "happy." A happy number is defined by the following process: Starting with any positive integer, replace the number by the sum of the squares of its digits, and repeat the process until the number equals 1 (where it will stay), or it loops endlessly in a cycle that does not include 1.

6. **Linked List Intersection**
   - Given the heads of two singly linked lists, return the node at which the two lists intersect. If the two linked lists have no intersection at all, return null.

7. **Rearrange a Linked List**
   - Given the head of a singly linked list, rearrange the list in such a way that it becomes sorted in alternating ascending and descending order.

8. **Palindrome Linked List**
   - Given the head of a singly linked list, determine if it is a palindrome.

9. **Circular Array Loop**
   - Given a circular array of integers, determine if there is a cycle in the array. A cycle must start and end at the same index and the cycle's length must be greater than 1. Moreover, movements in a cycle must all follow a single direction, either forward or backward.

10. **Find Duplicate Number**
    - Given an array of integers containing \( n + 1 \) integers where each integer is between 1 and \( n \) (inclusive), find the duplicate number. You must solve the problem without modifying the array and use only constant, \( O(1) \), extra space.
