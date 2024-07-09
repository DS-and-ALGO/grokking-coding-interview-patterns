## The Two Pointers Pattern

The two pointers pattern is a versatile technique used in problem-solving to efficiently traverse or manipulate sequential data structures, such as arrays or linked lists. As the name suggests, it involves maintaining two pointers that traverse the data structure in a coordinated manner, typically starting from different positions or moving in opposite directions. These pointers dynamically adjust based on specific conditions or criteria, allowing for the efficient exploration of the data and enabling solutions with optimal time and space complexity. Whenever there’s a requirement to find two data elements in an array that satisfy a certain condition, the two pointers pattern should be the first strategy to come to mind.

The pointers can be used to iterate through the data structure in one or both directions, depending on the problem statement. For example, to identify whether a string is a palindrome, we can use one pointer to iterate the string from the beginning and the other to iterate it from the end. At each step, we can compare the values of the two pointers and see if they meet the palindrome properties.

The naive approach to solving this problem would be using nested loops, with a time complexity of \(O(n^2)\). However, by using two pointers moving toward the middle from either end, we exploit the symmetry property of palindromic strings. This allows us to compare the elements in a single loop, making the algorithm more efficient with a time complexity of \(O(n)\).

### Examples

The following examples illustrate some problems that can be solved with this approach:

1. **Reversing an Array**: Given an array of integers, reverse it in place.

2. **Pair with Given Sum in a Sorted Array**: Given a sorted array of integers, find a pair in the array that sums to a number \(T\).

### Does Your Problem Match This Pattern?

Yes, if all of these conditions are fulfilled:

- **Linear Data Structure**: The input data can be traversed in a linear fashion, such as an array, linked list, or string.
- **Process Pairs**: Process data elements at two different positions simultaneously.
- **Dynamic Pointer Movement**: Both pointers move independently of each other according to certain conditions or criteria. In addition, both pointers might move along the same or two different data structures.

### Real-World Problems

Many problems in the real world use the two pointers pattern. Let’s look at an example.

**Memory Management**: The two pointers pattern is vital in memory allocation and deallocation. The memory pool is initialized with two pointers: the start pointer, pointing to the beginning of the available memory block, and the end pointer, indicating the end of the block. When a process or data structure requests memory allocation, the start pointer is moved forward, designating a new memory block for allocation. Conversely, when memory is released (deallocated), the start pointer is shifted backward, marking the deallocated memory as available for future allocations.



## DSA Questions Solvable with Two Pointers

1. **Two Sum II - Input Array Is Sorted**
   - Given a sorted array, find two numbers such that they add up to a specific target number. Return the indices of the two numbers.

2. **Remove Duplicates from Sorted Array**
   - Given a sorted array, remove the duplicates in-place such that each element appears only once and return the new length.

3. **Container With Most Water**
   - Given \(n\) non-negative integers representing an elevation map where the width of each bar is 1, find two lines that together with the x-axis form a container, such that the container contains the most water.

4. **Trapping Rain Water**
   - Given \(n\) non-negative integers representing an elevation map where the width of each bar is 1, compute how much water it can trap after raining.

5. **3Sum**
   - Given an array of integers, find all unique triplets in the array which gives the sum of zero.

6. **Palindrome Linked List**
   - Given the head of a singly linked list, determine if it is a palindrome.

7. **Subarray Product Less Than K**
   - Given an array of integers nums and an integer k, return the number of contiguous subarrays where the product of all the elements in the subarray is strictly less than k.

8. **Minimum Size Subarray Sum**
   - Given an array of positive integers nums and a positive integer target, return the minimal length of a contiguous subarray of which the sum is greater than or equal to target. If there is no such subarray, return 0 instead.

9. **Squares of a Sorted Array**
   - Given an array of integers sorted in non-decreasing order, return an array of the squares of each number sorted in non-decreasing order.

10. **Find the Longest Substring with At Most Two Distinct Characters**
    - Given a string, find the length of the longest substring that contains at most two distinct characters.
