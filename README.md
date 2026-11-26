
# Contains Duplicate

## Problem Description

Given an integer array `nums`, return `true` if any value appears more than once in the array. Otherwise, return `false`.

## Difficulty

🟢 Easy

## Topics

- Arrays
- Hash Sets
- Hash Tables
- Sorting

## Examples

### Example 1

**Input:**
```python
nums = [1, 2, 3, 3]
```

**Output:**
```python
True
```

**Explanation:** The number 3 appears more than once.

### Example 2

**Input:**
```python
nums = [1, 2, 3, 4]
```

**Output:**
```python
False
```

**Explanation:** Every element in the array is unique.

## Constraints

- `0 <= nums.length <= 10^5`
- `-10^9 <= nums[i] <= 10^9`

## Solution

The solution uses a set to keep track of the numbers that have already been visited.

```python
class Solution:
    def hasDuplicate(self, nums: List[int]) -> bool:
        seen = set()

        for i in nums:
            if i in seen:
                return True

            seen.add(i)

        return False
```

## Approach

1. Create an empty set called `seen`.
2. Iterate through each number in the array.
3. Check if the number already exists in the set.
4. If it exists, return `True`.
5. Otherwise, add the number to the set.
6. If no duplicates are found, return `False`.

## Complexity Analysis

| Complexity | Value |
|------------|-------|
| Time Complexity (Average) | O(n) |
| Space Complexity | O(n) |

Where `n` is the number of elements in the array.

## Key Takeaways

- Sets store unique values.
- Sets provide O(1) average lookup time.
- Returning early avoids unnecessary iterations.

## Problem Source

[NeetCode - Contains Duplicate](https://neetcode.io/problems/duplicate-integer)
