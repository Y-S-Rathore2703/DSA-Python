# 🔍 LeetCode 374 — Guess Number Higher or Lower

**Difficulty:** Easy | **Language:** Python | **Topic:** Binary Search

[Problem](https://leetcode.com/problems/guess-number-higher-or-lower/) · [My Solution](solution.py)

## Problem

A number is picked between `1` and `n`. Use the provided `guess(num)` API to find it.

- `-1`: The picked number is lower than our guess.
- `1`: The picked number is higher than our guess.
- `0`: We guessed correctly.

## Approach

Use Binary Search to reduce the search range by half in each iteration.

1. Start with `low = 1` and `high = n`.
2. Calculate the middle value: `mid = (low + high) // 2`.
3. Call `guess(mid)`.
4. If the result is `0`, return `mid`.
5. If the result is `-1`, search the left half by updating `high = mid - 1`.
6. If the result is `1`, search the right half by updating `low = mid + 1`.

## Key Concept

Binary Search eliminates half of the remaining search space after every guess.

## Complexity Analysis

- **Time Complexity:** O(log n) — the search range is halved each time.
- **Space Complexity:** O(1) — only a constant number of variables are used.

## Solution

See [solution.py](solution.py).

**Note:** The `guess()` API is provided by LeetCode; it does not need to be implemented.
