# Best Time to Buy and Sell Stock IV

## Problem
Given an integer array `prices` where `prices[i]` is the price of a stock on the `i-th` day, and an integer `k`.

Find the maximum profit you can achieve with at most `k` transactions.

You may not engage in multiple transactions simultaneously.

---

## Approach
This problem is solved using **Dynamic Programming + Recursion (Memoization)**.

### State Definition
We use:

- `ind` → current day
- `buy` → whether we can buy or sell
- `cap` → remaining transactions

### Choices
If `buy == 1`:
- Buy the stock
- Skip the day

If `buy == 0`:
- Sell the stock
- Skip the day

We store already computed states in a 3D DP array.

---

## Time Complexity
```text
O(N * 2 * K)
