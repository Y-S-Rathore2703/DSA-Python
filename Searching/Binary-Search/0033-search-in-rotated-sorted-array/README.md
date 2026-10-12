# 🔎 LeetCode 33 — Search in Rotated Sorted Array

**Difficulty:** Medium | **Language:** Python | **Topic:** Binary Search

[Problem](https://leetcode.com/problems/search-in-rotated-sorted-array/) · [My Solution](solution.py)

## Problem

An array that was originally sorted in ascending order has been rotated at an unknown pivot. Given the rotated array `nums` and an integer `target`, return the index of `target` if it exists. Otherwise, return `-1`.

The solution must run in **O(log n)** time.

## Approach

Even after rotation, at least one half of the current search range is always sorted.

1. Calculate the middle index.
2. If the middle element is the target, return its index.
3. Check whether the left half is sorted using `nums[low] <= nums[mid]`.
4. If the target falls inside that sorted half, search it; otherwise, search the other half.
5. Repeat until the target is found or the search range becomes empty.

## Example

```python
nums = [4, 5, 6, 7, 0, 1, 2]
target = 0

# Output: 4
```

## Key Concept

A rotated sorted array is not completely sorted, but one side of the middle is always sorted. Use that sorted half to decide which direction to continue searching.

## Complexity Analysis

- **Time Complexity:** O(log n) — the search range is halved in each iteration.
- **Space Complexity:** O(1) — only a constant amount of extra space is used.

## Solution

See [solution.py](solution.py).
