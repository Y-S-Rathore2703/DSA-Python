# 🔍 LeetCode 278 — First Bad Version

**Difficulty:** Easy | **Language:** Python | **Topic:** Binary Search

[Problem](https://leetcode.com/problems/first-bad-version/) · [My Solution](solution.py)

## Problem

You are given `n) versions of a product. Some version is the first bad version, and every version after it is also bad.

Use the `isBadVersion(version)` API to find and return the **first bad version**.

## Approach — Binary Search

1. Set `low = 1` and `high = n`.
2. Calculate the middle version: `mid = (low + high) // 2`.
3. Check `isBadVersion(mid)`:
   - If it is `True`, the first bad version is at `mid) or somewhere to its left. Set `high = mid - 1`.
   - If it is `False`, the first bad version must be to its right. Set `low = mid + 1`.
4. Continue until `low > high`. At that point, `low` is the first bad version.

## Key Concept

This is a **boundary-search** problem. We are not looking for just any bad version; we need the earliest one. When the search ends, `high` is the last good version and `low` is the first bad version.

## Complexity Analysis

- **Time Complexity:** `O(log n)` — each check eliminates about half of the remaining versions.
- **Space Complexity:** `O(1)` — only a fixed number of variables are used.

## Solution

See [solution.py](solution.py).
