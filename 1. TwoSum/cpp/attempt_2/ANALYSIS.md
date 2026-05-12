# 1. Two Sum — C++ Attempt #2

## Complexity Analysis
Analyse THIS specific solution. For Time and Space complexity each:
- Time complexity: **O(n)**, because the solution iterates over the `nums` array once using a `for` loop (`for(int i = 0; i<nums.size();i++)`), and the operations inside the loop (looking up in `mymap` and inserting into `mymap`) take constant time on average.
- Space complexity: **O(n)**, because in the worst case, the solution stores every element from the `nums` array in the `mymap` (`mymap[nums[i]] = i;`).

## Code Feedback
Two subsections:

### Strengths
* The solution uses an `unordered_map` to store the numbers and their indices, which allows for efficient lookups.
* The solution only iterates over the `nums` array once, which minimizes the time complexity.
* The solution returns as soon as it finds a pair of numbers that add up to the target, which avoids unnecessary iterations.

### Suggestions
* Consider adding a check for an empty `nums` array to handle edge cases: `if (nums.empty()) return {};`.
* The solution is already optimal in terms of time complexity, but it could be improved by adding more comments to explain the logic: `// Check if the complement of the current number is in the map`.
* The variable name `mymap` could be more descriptive, such as `numToIndexMap`: `unordered_map<int, int> numToIndexMap;`.

## Approaches
### Brute Force
The brute force approach involves iterating over the `nums` array and checking every pair of numbers to see if they add up to the target. Time complexity: **O(n^2)**, Space complexity: **O(1)**, Example: `for (int i = 0; i < nums.size(); i++) { for (int j = i + 1; j < nums.size(); j++) { if (nums[i] + nums[j] == target) return {i, j}; } }`.
### Hash Table (your solution)
The hash table approach involves using a map to store the numbers and their indices, and then looking up the complement of each number in the map. Time complexity: **O(n)**, Space complexity: **O(n)**, Example: `unordered_map<int, int> numToIndexMap; for (int i = 0; i < nums.size(); i++) { if (numToIndexMap.count(target - nums[i])) return {i, numToIndexMap[target - nums[i]]}; numToIndexMap[nums[i]] = i; }`.
### Sorting
The sorting approach involves sorting the `nums` array and then using two pointers to find a pair of numbers that add up to the target. Time complexity: **O(n log n)**, Space complexity: **O(n)**, Example: `sort(nums.begin(), nums.end()); int left = 0, right = nums.size() - 1; while (left < right) { if (nums[left] + nums[right] == target) return {left, right}; else if (nums[left] + nums[right] < target) left++; else right--; }`.
