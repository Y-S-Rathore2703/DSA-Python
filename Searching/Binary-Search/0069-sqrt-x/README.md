# 🔎 LeetCode 69 — Sqrt(x)

**Difficulty:** Easy | **Language:** Python | **Topic:** Binary Search

[Problem](https://leetcode.com/problems/sqrtx/) · [My Solution](solution.py)

## Problem

Given a non-negative integer `x`, return the square root of `x` rounded down to the nearest integer.

You are not allowed to use built-in exponent functions or the `sqrt()` function.

## Approach — Binary Search

Instead of checking every number, use Binary Search to find the largest integer whose square is less than or equal to `x`.

1. Initialise `low = 0` and `high = x`.
2. Calculate the middle value using `(low + high) // 2`.
3. Calculate its square using `mid * mid`.
4. If the square equals `x`, return `mid`.
5. If the square is smaller than `x`, search the right half.
6. If the square is greater than `x`, search the left half.
7. When the search ends, return `high`.

## Key Concept

In this problem, `mid` represents a possible answer rather than an array index.

- `square < x` → Move right using `low = mid + 1`.
- `square > x` → Move left using `high = mid - 1`.
- `square == x` → Return `mid`.

When Binary Search terminates, `high` represents the largest integer whose square is less than or equal to `x`.

## Complexity Analysis

- **Time Complexity:** O(log x) — The search space is halved in every iteration.
- **Space Complexity:** O(1) — Only a constant amount of extra space is used.

## Solution

See [solution.py](solution.py).
