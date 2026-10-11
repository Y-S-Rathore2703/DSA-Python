# 🔎 LeetCode 367 — Valid Perfect Square

**Difficulty:** Easy | **Language:** Python | **Topic:** Binary Search

[Problem](https://leetcode.com/problems/valid-perfect-square/) · [My Solution](solution.py)

## Problem

Given a positive integer `num`, determine whether it is a perfect square. A perfect square is an integer that can be written as the product of an integer multiplied by itself.

Do not use built-in square-root functions.

## Approach — Binary Search

Use Binary Search to find an integer whose square equals `num`.

1. Initialise `low = 0` and `high = num`.
2. While `low <= high`, calculate `mid = (low + high) // 2`.
3. Calculate `square = mid * mid`.
4. If `square == num`, return `True`.
5. If `square < num`, search the right half by updating `low = mid + 1`.
6. If `square > num`, search the left half by updating `high = mid - 1`.
7. If the loop ends without finding an exact square, return `False`.

## Key Concept

A perfect square must have an integer whose square is exactly equal to `num`.

- `square == num` → The number is a perfect square.
- `square < num` → The possible integer is larger, so move right.
- `square > num` → The possible integer is smaller, so move left.
- If Binary Search finishes without an exact match, the number is not a perfect square.

Calculate a new `mid` and `square` inside every loop iteration because `low` and `high` change.

## Complexity Analysis

- **Time Complexity:** O(log num) — The search space is halved in every iteration.
- **Space Complexity:** O(1) — Only a constant amount of extra space is used.

## Solution

See [solution.py](solution.py).
