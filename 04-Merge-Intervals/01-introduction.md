## Merge Intervals Pattern

The merge intervals pattern deals with problems involving overlapping intervals. Each interval is represented by a start and an end time. For example, an interval of `[10, 20]` seconds means that the interval starts at 10 seconds and ends at 20 seconds. This pattern involves tasks such as merging intersecting intervals, inserting new intervals into existing sets, or determining the minimum number of intervals needed to cover a given range. The most common problems solved using this pattern are event scheduling, resource allocation, and time slot consolidation.

The key to understanding this pattern and exploiting its power lies in understanding how any two intervals may overlap. The illustration below shows different ways in which two intervals can relate to each other:

Press
+
to interact

canvasAnimation-image

1 of 3

## Step-by-Step Guide

1. **Identify the Problem Requirements**
   - Determine that the problem involves working with intervals and whether the task is to merge, insert, or evaluate intervals.
   - **Explanation**: Recognize that you will need to sort intervals and then compare them to manage overlaps.

2. **Sort the Intervals**
   - Sort the intervals by their start times (and by end times if necessary for tie-breaking).
   - **Explanation**: Sorting ensures that intervals are considered in chronological order, which is essential for efficiently merging overlapping intervals.
   - **Supporting Links**: [Sorting Algorithms](https://www.geeksforgeeks.org/sorting-algorithms/)

3. **Merge Overlapping Intervals**
   - Traverse the sorted list and merge overlapping intervals.
   - **Explanation**: Compare the current interval with the next one to check for overlaps. Merge intervals as necessary and update the result list.
   - **Supporting Links**: [Merge Intervals](https://leetcode.com/problems/merge-intervals/)

4. **Handle Edge Cases**
   - Ensure that edge cases like non-overlapping intervals or intervals that are subsets of each other are handled properly.
   - **Explanation**: Consider scenarios where no intervals overlap or where intervals are nested within each other.

5. **Return the Result**
   - Return the list of merged intervals or the result of the interval operation.
   - **Explanation**: After processing all intervals, return the final list of intervals or the required result based on the problem statement.

## Examples

1. **Merge Intervals**
   - Given a sorted list of intervals, merge all overlapping intervals.
   - **Explanation**: Use the sliding window approach to combine overlapping intervals into a single interval.
   - **Supporting Links**: [Merge Intervals Problem](https://leetcode.com/problems/merge-intervals/)

2. **Meeting Rooms**
   - Given an array of meeting time intervals consisting of start and end times, determine if a person could attend all meetings.
   - **Explanation**: Check if there are any overlaps between meetings by analyzing the intervals.
   - **Supporting Links**: [Meeting Rooms Problem](https://leetcode.com/problems/meeting-rooms/)

## Does Your Problem Match This Pattern?

Yes, if both of these conditions are fulfilled:

- **Array of Intervals**: The input data is an array of intervals.
- **Overlapping Intervals**: The problem requires dealing with overlapping intervals, either to find their union, their intersection, or the gaps between them.

## Real-World Problems

1. **Display Busy Schedule**
   - Display the busy hours of a user to other users without revealing the individual meeting slots in a calendar.
   - **Explanation**: Merge overlapping meeting times to show the user’s busy periods.

2. **Schedule a New Meeting**
   - Add a new meeting to the tentative meeting schedule of a user in such a way that no two meetings overlap each other.
   - **Explanation**: Insert a new interval into an existing schedule and ensure no conflicts.

3. **Task Scheduling in Operating Systems (OS)**
   - Schedule tasks for the OS based on task priority and the free slots in the machine’s processing schedule.
   - **Explanation**: Manage tasks by merging intervals to find available time slots and prioritize tasks.



## DSA Problems Solvable with Merge Intervals Pattern

1. **[Merge Intervals](https://leetcode.com/problems/merge-intervals/)**
   - **Description**: Given a collection of intervals, merge all overlapping intervals.
   - **Example**: Input: `[[1,3],[2,6],[8,10],[15,18]]`  
     Output: `[[1,6],[8,10],[15,18]]`

2. **[Meeting Rooms](https://leetcode.com/problems/meeting-rooms/)**
   - **Description**: Determine if a person can attend all meetings given a list of meeting time intervals.
   - **Example**: Input: `[[0,30],[5,10],[15,20]]`  
     Output: `false`

3. **[Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/)**
   - **Description**: Given a collection of meeting time intervals, find the minimum number of conference rooms required.
   - **Example**: Input: `[[0,30],[5,10],[15,20]]`  
     Output: `2`

4. **[Insert Interval](https://leetcode.com/problems/insert-interval/)**
   - **Description**: Insert a new interval into a sorted list of non-overlapping intervals and merge if necessary.
   - **Example**: Input: `[[1,3],[6,9]], newInterval = [2,5]`  
     Output: `[[1,5],[6,9]]`

5. **[Interval List Intersections](https://leetcode.com/problems/interval-list-intersections/)**
   - **Description**: Given two lists of intervals, find the intersections between the two lists.
   - **Example**: Input: `A = [[0,2],[5,10],[13,23],[24,25]], B = [[1,5],[8,12],[15,24],[25,26]]`  
     Output: `[[1,2],[5,5],[8,10],[15,23],[24,24]]`

6. **[Non-overlapping Intervals](https://leetcode.com/problems/non-overlapping-intervals/)**
   - **Description**: Find the minimum number of intervals you need to remove to make the rest of the intervals non-overlapping.
   - **Example**: Input: `[[1,2],[2,3],[3,4],[1,3]]`  
     Output: `1`

7. **[Find Minimum Number of Meeting Rooms](https://www.geeksforgeeks.org/find-minimum-number-meeting-rooms-required/)**
   - **Description**: Find the minimum number of meeting rooms required to accommodate all meetings.
   - **Example**: Input: `[[0,30],[5,10],[15,20]]`  
     Output: `2`

8. **[Employee Free Time](https://leetcode.com/problems/employee-free-time/)**
   - **Description**: Given a collection of employee schedules, find the free time intervals for all employees.
   - **Example**: Input: `[[[1,2],[5,6]],[[1,3]],[[2,3],[6,8]]]`  
     Output: `[[3,5],[8,9]]`

9. **[Calendar Intersection](https://leetcode.com/problems/calendar-intersection/)**
   - **Description**: Given two calendars, find the common time intervals when both calendars are free.
   - **Example**: Input: `A = [[1,3],[6,9]], B = [[2,5],[8,10]]`  
     Output: `[[2,3],[8,9]]`

10. **[Task Scheduler](https://www.geeksforgeeks.org/task-scheduler/)**
    - **Description**: Schedule tasks with given intervals and a cooldown period between the same tasks.
    - **Example**: Input: `tasks = ["A","A","A","B","B","B"], n = 2`  
      Output: `8` (The tasks can be scheduled as A-B-C-A-B-C-A-B-C)

## Summary

The merge intervals pattern is applicable in various scenarios, including scheduling problems, managing overlapping tasks, and optimizing resource allocations. Understanding and applying this pattern can help solve a range of problems related to time management and interval overlap.

