# 1. Two Sum — C++ Attempt #1

## Complexity Analysis
Analyse THIS specific solution. For Time and Space complexity each:
- Time complexity: **O(n)**, because the solution iterates over the `nums` array once using a `for` loop (`for(int i = 0; i<nums.size();i++)`), and the operations inside the loop (looking up in the `unordered_map` and inserting into it) take constant time on average.
- Space complexity: **O(n)**, because in the worst case, the solution stores every element of the `nums` array in the `mymap` (`unordered_map<int,int> mymap;`), which requires linear space.

## Code Feedback
Two subsections:

### Strengths
* The solution uses an `unordered_map` to store the elements of the `nums` array and their indices, allowing for efficient lookups.
* The solution only iterates over the `nums` array once, making it efficient.
* The solution returns as soon as it finds a pair of elements that add up to the target, which minimizes unnecessary work.

### Suggestions
* The solution could benefit from more descriptive variable names, such as `numToIndexMap` instead of `mymap`.
* The solution could include a check for an empty `nums` array to handle this edge case explicitly: `if (nums.empty()) { return {}; }`.
* The solution is already optimal, so no further improvements are needed.

## Approaches
### Brute Force
- Idea: Check every pair of elements in the `nums` array to see if they add up to the target.
- Time complexity: **O(n^2)**, Space complexity: **O(1)**
- Code snippet: `for (int i = 0; i < nums.size(); i++) { for (int j = i + 1; j < nums.size(); j++) { if (nums[i] + nums[j] == target) { return {i, j}; } } }`

### Hash Table (your solution)
- Idea: Use a hash table to store the elements of the `nums` array and their indices, and look up the complement of each element in the hash table.
- Time complexity: **O(n)**, Space complexity: **O(n)**
- Code snippet: `unordered_map<int, int> numToIndexMap; for (int i = 0; i < nums.size(); i++) { if (numToIndexMap.count(target - nums[i])) { return {i, numToIndexMap[target - nums[i]]}; } numToIndexMap[nums[i]] = i; }`

### Sorting
- Idea: Sort the `nums` array and use two pointers to find a pair of elements that add up to the target.
- Time complexity: **O(n log n)**, Space complexity: **O(n)**
- Code snippet: `sort(nums.begin(), nums.end()); int left = 0, right = nums.size() - 1; while (left < right) { if (nums[left] + nums[right] == target) { return {left, right}; } else if (nums[left] + nums[right] < target) { left++; } else { right--; } }`
