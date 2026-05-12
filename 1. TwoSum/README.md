# 1. Two Sum

**Difficulty:** 🟢 Easy

**Link:** [LeetCode Problem](https://leetcode.com/problems/two-sum/)

---

## Solutions

| Language | Runtime | Memory | Time | Date |
|----------|---------|--------|------|------|
| C++ | 3 ms (66.5%) | 14.8 MB (36.7%) | 01:15 | 2026-05-09 |
| C++ | 2 ms (71.6%) | 14.7 MB (63.3%) | 00:06 | 2026-05-11 |
| C++ | 3 ms (66.4%) | 14.8 MB (36.7%) | 00:12 | 2026-05-12 |
| C++ | 2 ms (71.6%) | 14.8 MB (54.2%) | - | 2026-05-12 |
| C++ | 0 ms (100.0%) | 15 MB (18.1%) | - | 2026-05-12 |
| C++ | 3 ms (66.4%) | 14.9 MB (18.1%) | - | 2026-05-12 |
| C++ | 2 ms (71.6%) | 14.7 MB (54.2%) | - | 2026-05-12 |
| C++ | 4 ms (51.4%) | 14.9 MB (36.7%) | - | 2026-05-12 |
| C++ | 3 ms (66.4%) | 14.8 MB (36.7%) | - | 2026-05-12 |
| C++ | 0 ms (100.0%) | 15 MB (18.1%) | - | 2026-05-12 |
| C++ | 2 ms (71.6%) | 14.9 MB (36.7%) | - | 2026-05-12 |

## Complexity Analysis
* Time complexity: O(n), where n is the number of elements in the input array, because we are doing a single pass through the array.
* Space complexity: O(n), where n is the number of elements in the input array, because in the worst case, we might need to store all elements in the hashmap.

## Approaches
### Brute Force Approach
This approach involves checking every pair of elements in the array to see if they add up to the target sum.
* Time complexity: O(n^2)
* Space complexity: O(1)
### Hash Table Approach
This approach involves using a hash table to store the elements we have seen so far and their indices, and checking if the difference between the target and the current element is in the hash table.
* Time complexity: O(n)
* Space complexity: O(n)
### Optimized Hash Table Approach
This approach is the same as the hash table approach, but with some minor optimizations such as using a more efficient hash function or handling edge cases more efficiently.
* Time complexity: O(n)
* Space complexity: O(n)
| C++ | 0 ms (100.0%) | 14.9 MB (18.1%) | - | 2026-05-12 |
| C++ | 3 ms (66.4%) | 14.8 MB (54.2%) | - | 2026-05-12 |
