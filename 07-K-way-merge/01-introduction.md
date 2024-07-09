## K-Way Merge Pattern

The K-way merge pattern is an essential algorithmic strategy for merging K sorted data structures, such as arrays and linked lists, into a single sorted data structure. This technique is an expansion of the standard merge sort algorithm, which traditionally merges two sorted data structures into one.

**Note:** For simplicity, we’ll use the term *lists* to refer to arrays and linked lists in our discussion.

### Understanding the K-Way Merge Algorithm

The K-way merge algorithm works by repeatedly selecting the smallest (or largest, if we’re sorting in descending order) element from among the first elements of the K input lists and adding this element to a new output list (with the same data type as the inputs). This process is repeated until all elements from all input lists have been merged into the output list, maintaining the sorted order.

Here are two main approaches to achieve the K-way merge:

### Approach 1: Using a Min Heap

1. **Insert the First Elements**:
   - Insert the first element of each list into a min heap. This sets up our starting point, with the heap helping us efficiently track the smallest current element among the lists.
   - **Explanation**: The min heap is used to always retrieve the smallest element among the first elements of the K lists.
   - **Supporting Links**: [Min Heap Data Structure](https://www.geeksforgeeks.org/min-heap-or-min-priority-queue/)

2. **Remove the Smallest Element**:
   - Remove the smallest element from the heap (which is always at the top) and add it to the output list. This ensures that our output list is being assembled in sorted order.
   - **Explanation**: The smallest element is added to the final merged list, maintaining sorted order.

3. **Track the Source**:
   - Keep track of which list each element in the heap came from. This is for knowing where to find the next element to add to the heap.
   - **Explanation**: Each element’s origin helps fetch the next element from the same list.

4. **Replace with the Next Element**:
   - After removing the smallest element from the heap and adding it to the output list, replace it with the next element from the same list the removed element belonged to.
   - **Explanation**: This step ensures the heap always has the smallest element from each list.

5. **Repeat**:
   - Repeat steps 2-4 until all elements from all input lists have been merged into the output list.
   - **Explanation**: Continue until the heap is empty and all elements are added to the merged list.
   - **Supporting Links**: [Heap Operations](https://www.geeksforgeeks.org/heap-data-structure/)

### Approach 2: Grouping and Merging Pairs of Lists

1. **Divide into Pairs**:
   - Start by dividing the K sorted lists into pairs, making groups of two. This organizes our lists into manageable units for merging.
   - **Explanation**: The division helps manage the merging process by reducing it to a series of two-way merges.

2. **Merge Each Pair**:
   - For each pair of lists, perform a standard two-way merge operation. This is similar to the merge step in merge sort, where two sorted lists are combined into a single sorted list.
   - **Explanation**: This step results in \( k/2 \) merged lists.

3. **Handle Odd Numbers**:
   - If there are an odd number of lists in a group at any point, simply leave one list unmerged in that round.
   - **Explanation**: Ensure no list is left out of the merging process.

4. **Repeat the Process**:
   - Repeat the process of pairing up the resulting lists from the previous merge and merging them again until only one sorted list remains.
   - **Explanation**: Continue until only one list remains, which is the final result.

### Examples

The following examples illustrate some problems that can be solved with this approach:

1. **[Median of K Sorted Arrays](https://leetcode.com/problems/median-of-k-sorted-arrays/)**
   - **Description**: Find the median of the \( k \) sorted arrays.
   - **Example**: Input: `[[1, 6, 8, 12], [3, 6, 7], [1, 3, 4, 5, 9], [1, 6, 7]]`  
     Output: `[1, 1, 1, 3, 4, 5, 6, 6, 6, 7, 7, 8, 9, 12]`

2. **[Kth Smallest Element in Multiple Sorted Arrays](https://leetcode.com/problems/kth-smallest-element-in-multiple-sorted-arrays/)**
   - **Description**: Find the \( k \)-th smallest element of multiple sorted arrays.
   - **Example**: Input: `[[1, 6, 8, 12], [3, 6, 7], [1, 3, 4, 5, 9], [1, 6, 7]], k=4`  
     Output: `4`

3. **[Merge K Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists/)**
   - **Description**: Merge \( k \) sorted linked lists into one sorted linked list.
   - **Example**: Input: `[[1,4,5],[1,3,4],[2,6]]`  
     Output: `[1,1,2,3,4,4,5,6]`

4. **[Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/)**
   - **Description**: Merge two sorted arrays into a single sorted array.
   - **Example**: Input: `[1,2,3,0,0,0], m=3, n=3`  
     Output: `[1,2,2,3,5,6]`

5. **[Kth Largest Element in an Array](https://leetcode.com/problems/kth-largest-element-in-an-array/)**
   - **Description**: Find the \( k \)-th largest element in an unsorted array.
   - **Example**: Input: `[3,2,1,5,6,4], k=2`  
     Output: `5`

6. **[K Closest Points to Origin](https://leetcode.com/problems/k-closest-points-to-origin/)**
   - **Description**: Find the \( k \) closest points to the origin from a list of points.
   - **Example**: Input: `[[1,3],[-2,2]], K=1`  
     Output: `[[-2,2]]`

7. **[Merge Intervals](https://leetcode.com/problems/merge-intervals/)**
   - **Description**: Merge all overlapping intervals.
   - **Example**: Input: `[[1,3],[2,6],[8,10],[15,18]]`  
     Output: `[[1,6],[8,10],[15,18]]`

8. **[Find All Anagrams in a String](https://leetcode.com/problems/find-all-anagrams-in-a-string/)**
   - **Description**: Find all start indices of anagrams of a given string in a string.
   - **Example**: Input: `s="cbaebabacd", p="abc"`  
     Output: `[0, 6]`

9. **[Search a 2D Matrix II](https://leetcode.com/problems/search-a-2d-matrix-ii/)**
   - **Description**: Write an efficient algorithm that searches for a value in an m x n matrix.
   - **Example**: Input: `matrix=[[1,4,7,11],[2,5,8,12],[3,6,9,16],[10,13,14,17]]`, target=5`Output:`true`

10. **[Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/)**
    - **Description**: Merge two sorted arrays into a single sorted array.
    - **Example**: Input: `nums1 = [1,2,3,0,0,0], m = 3, nums2 = [2,5,6], n = 3`  
      Output: `[1,2,2,3,5,6]`

### Does Your Problem Match This Pattern?

Yes, if one or both of the following conditions are fulfilled:

- **Involves Merging Sorted Arrays or a Matrix**:
  - The problem involves a collection of sorted arrays or a matrix with rows or columns sorted in a specific order that needs to be merged. This could be the core of the problem or a step toward the solution.
  
- **Seeking the K-th Smallest/Largest Across Sorted Collections**:
  - The problem involves identifying the \( k \)-th smallest or largest element across multiple sorted arrays or linked lists.

### Real-World Problems

1. **Patient Records Aggregation**
   - **Description**: In healthcare informatics, patient data often come from multiple sources, such as lab results, physician notes, and imaging reports, each sorted by date or priority. Integrating these data streams into a single, chronologically ordered patient record is essential for providing comprehensive care. The K-way merge pattern can efficiently combine these sorted data streams, ensuring doctors and nurses have timely access to a unified view of patient history, which is
