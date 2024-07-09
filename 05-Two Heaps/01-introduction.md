## Two Heaps Pattern

The two heaps pattern is a versatile and efficient approach used to solve problems involving dynamic data processing, optimization, and real-time analysis. As the name suggests, this pattern maintains two heaps, which could be either two min heaps, two max heaps, or a min heap and a max heap. Exploiting the heap property, the two heaps pattern is a preferred technique for various problems to implement computationally efficient solutions. For a heap containing \( n \) elements, inserting or removing an element takes \( O(\log n) \) time, while accessing the element at the root is done in \( O(1) \) time. The root stores the smallest element in the case of a min heap and the largest element in the case of a max heap.

Let’s explore a few example scenarios to gain a better understanding. In some problems, we’re given a dataset and tasked to divide it into two parts to find the smallest value from one part and the largest value from the other part. To achieve this, we can build two heaps: one min heap and one max heap, from these two subsets of data. The root of the min heap will give us the smallest value from its corresponding dataset, while the root of the max heap will provide the largest value from its dataset. In cases where we need to find the two largest numbers from two different datasets, we’ll use two max heaps to store and manage these datasets. Similarly, to find the two smallest numbers from two different datasets, we would use two min heaps. These examples illustrate the versatility of using min heaps and max heaps to efficiently solve different types of problems by facilitating quick access to the smallest or largest values as required.

The following illustration demonstrates how we can build a min heap or a max heap, and how they can be used to solve several tasks, e.g., finding the smallest or largest element from some data:

Press
+
to interact

canvasAnimation-image

1 of 13

## Step-by-Step Guide

1. **Identify the Problem Requirements**
   - Determine if the problem involves maintaining or processing dynamic data where you need to frequently access the smallest or largest elements.
   - **Explanation**: Understand if you need to manage two separate datasets or two views of the same dataset to find minimum and maximum values or medians.

2. **Choose the Heap Types**
   - Decide on the heap types based on the problem’s needs: use two min heaps, two max heaps, or a combination of one min heap and one max heap.
   - **Explanation**: Select the heap types depending on whether you need to find maxima/minima or maintain a running median.
   - **Supporting Links**: [Heap Data Structure](https://www.geeksforgeeks.org/heap-data-structure/)

3. **Implement the Heaps**
   - Construct the heaps as required: for example, use a max heap to store the lower half of the data and a min heap to store the upper half.
   - **Explanation**: Implement the heaps to manage the datasets, ensuring that the heaps are maintained properly after each insertion or removal.
   - **Supporting Links**: [Implementing Heaps](https://www.geeksforgeeks.org/heap-data-structure/)

4. **Manage Heap Operations**
   - Perform heap operations like insertion, deletion, and root access efficiently to maintain the required properties of the heaps.
   - **Explanation**: Ensure that the heaps are balanced and their properties are preserved after each operation.
   - **Supporting Links**: [Heap Operations](https://www.geeksforgeeks.org/heap-data-structure/)

5. **Perform Calculations**
   - Use the heaps to perform calculations such as finding the median, or finding the minimum and maximum values from two datasets.
   - **Explanation**: Extract the necessary information from the heaps as per the problem requirements.
   - **Supporting Links**: [Heap Applications](https://www.geeksforgeeks.org/applications-of-heap-data-structure/)

## Examples

1. **[Sliding Window Median](https://leetcode.com/problems/sliding-window-median/)**
   - **Description**: Given an array of integers and a window size \( k \), find the median of each sliding window of size \( k \) as it moves from left to right through the array.
   - **Example**: Input: `[1,3,-1,-3,5,3,6,7], k = 3`  
     Output: `[1, -1, -1, 3, 5, 6]`

2. **[Find Median from Data Stream](https://leetcode.com/problems/find-median-from-data-stream/)**
   - **Description**: Given a continuous stream of numbers, find the median of the numbers seen so far after any insertion in constant time.
   - **Example**: Input: `1, 2, 3`  
     Output: `2.0`

3. **[Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/)**
   - **Description**: Given a non-empty array of integers, return the \( k \) most frequent elements.
   - **Example**: Input: `[1,1,1,2,2,3], k = 2`  
     Output: `[1, 2]`

4. **[Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/)**
   - **Description**: Find the median of two sorted arrays.
   - **Example**: Input: `[1, 3], [2]`  
     Output: `2.0`

5. **[Find K Pairs with Smallest Sums](https://leetcode.com/problems/find-k-pairs-with-smallest-sums/)**
   - **Description**: Find the \( k \) pairs with the smallest sums from two integer arrays.
   - **Example**: Input: `A = [1,7,11], B = [2,4,6], k = 3`  
     Output: `[[1,2],[1,4],[1,6]]`

6. **[Kth Largest Element in a Stream](https://leetcode.com/problems/kth-largest-element-in-a-stream/)**
   - **Description**: Find the \( k \)-th largest element in a stream of integers.
   - **Example**: Input: `stream = [4, 5, 8, 2], k = 3`  
     Output: `5`

7. **[Add and Search Word - Data structure Design](https://leetcode.com/problems/add-and-search-word-data-structure-design/)**
   - **Description**: Design a data structure that supports adding new words and searching for a word with a given prefix.
   - **Example**: Input: `["addWord","search","search","search","search"], ["bad","bad..","bad.d","b..d","badd"]`  
     Output: `[null, true, true, false, true]`

8. **[Stream of Characters](https://leetcode.com/problems/stream-of-characters/)**
   - **Description**: Implement a stream of characters and check if it matches any word from a dictionary.
   - **Example**: Input: `["a","b","c","a","b","d"], word = "abc"`  
     Output: `true`

9. **[K Closest Points to Origin](https://leetcode.com/problems/k-closest-points-to-origin/)**
   - **Description**: Find the \( k \) closest points to the origin from a list of points.
   - **Example**: Input: `points = [[1,3],[-2,2]], K = 1`  
     Output: `[[-2,2]]`

10. **[Rearrange String k Distance Apart](https://leetcode.com/problems/rearrange-string-k-distance-apart/)**
    - **Description**: Rearrange the string so that the same characters are at least \( k \) distance apart.
    - **Example**: Input: `str = "aabbcc", k = 3`  
      Output: `"abcabc"`

## Does Your Problem Match This Pattern?

Yes, if both of these conditions are fulfilled:

- **Static or Streaming Data**: The input could either be linear data or a continuous stream of data.
- **Maxima and Minima Calculation**: The input data can be categorized into two parts, and you need to repeatedly calculate two maxima, two minima, or one maximum and one minimum from the two sets, respectively.

## Real-World Problems

1. **Video Platforms**
   - **Description**: As part of a demographic study, we’re interested in the median age of the viewers. We want to implement a functionality whereby the median age can be updated efficiently whenever a new user signs up for video streaming.
   - **Explanation**: Maintain a min heap and a max heap to track the median age of viewers.

2. **Gaming Matchmaking**
   - **Description**: Matching players of similar skill levels is crucial for a balanced and enjoyable gaming experience. By maintaining two heaps (one for minimum skill level and one for maximum skill level), matchmaking algorithms can efficiently pair players based on their skill levels.
   - **Explanation**: Use heaps to manage player skill levels and match players based on the closest skill levels.

