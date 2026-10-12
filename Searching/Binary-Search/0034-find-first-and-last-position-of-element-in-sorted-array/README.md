# 🔍 LeetCode 34 — Find First and Last Position of Element in Sorted Array

**Difficulty:** Medium | **Language:** Python | **Topic:** Binary Search

[Problem](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/) · [My Solution](solution.py)

## Problem

Given a sorted array of integers `nums` and a target value, find the starting and ending position of the target.

If the target is not found, return `[-1, -1]`.

## Approach — Two Binary Searches

We use Binary Search twice because we need both boundaries of the target:

1. **Find the first occurrence:**
   - If `nums[mid] == target`, save `mid` in `first`.
   - Continue searching left with `high = mid - 1` to find an earlier occurrence.
2. **Find the last occurrence:**
   - If `nums[mid] == target`, save `mid` in `last`.
   - Continue searching right with `low = mid + 1` to find a later occurrence.
3. If the target does not exist, the saved positions remain `-1`.
4. Return `[findFirst(), findLast()]`.

## Example

**Input:** `nums = [5, 7, 7, 8, 8, 10]`, `target = 8`

**Output:** `[3, 4]`

## Key Concept

When searching for the **first occurrence**, keep moving left after finding the target. When searching for the **last occurrence**, keep moving right.

## Complexity Analysis

- **Time Complexity:** `O(log n)` — two Binary Searches, each taking logarithmic time.
- **Space Complexity:** `O(1)` — only a fixed number of extra variables are used.

## Solution

See [solution.py](solution.py).
