# 🔎 LeetCode 35 — Search Insert Position

**Difficulty:** Easy | **Language:** Python | **Topic:** Binary Search

[Problem](https://leetcode.com/problems/search-insert-position/) · [My Solution](solution.py)

## Problem

Given a sorted array of distinct integers and a target value, return the index if the target exists.

If it doesn't exist, return the index where it should be inserted to maintain sorted order.

## Approach — Binary Search

1. Initialise `low = 0` and `high = len(nums) - 1`.
2. Calculate the middle index using `(low + high) // 2`.
3. If the middle element equals the target, return its index.
4. If the middle element is smaller than the target, search the right half.
5. If the middle element is greater than the target, search the left half.
6. If the target is not found, return `low` as the insertion position.

## Key Concept

When binary search terminates, `low` represents the correct insertion position.

- `return mid` → Target found.
- `return low` → Target not found; return its insertion index.

## Complexity Analysis

- **Time Complexity:** O(log n) — Search space is halved in every iteration.
- **Space Complexity:** O(1) — Only a constant amount of extra space is used.

## Solution

See [solution.py](solution.py).
