# leet-day43

# Longest Chain of Pairs

This program solves the "Longest Chain of Pairs" problem, where you are given an array of pairs, and you need to find the length of the longest chain that can be formed by following a specific rule.

## Problem Description

You are given an array of `n` pairs `pairs`, where `pairs[i] = [lefti, righti]` and `lefti < righti`. A pair `p2 = [c, d]` follows a pair `p1 = [a, b]` if `b < c`. A chain of pairs can be formed in this fashion. The goal is to find the length of the longest chain that can be formed using the provided pairs.

## Solution Approach

The solution to this problem involves sorting the pairs based on their ending values and then iteratively checking whether a chain can be formed using the current pair. The following steps outline the solution approach:

1. Sort the pairs based on their ending values. This helps to ensure that pairs with smaller ending values come first, making it easier to form chains.

2. Initialize two variables: `count` to keep track of the length of the longest chain, and `end` to keep track of the ending value of the previous pair.

3. Iterate through the sorted pairs. For each pair, compare its starting value with the current `end`. If the starting value is greater than `end`, it means a chain can be extended. Increment the `count` and update the `end` to the ending value of the current pair.

4. After iterating through all the pairs, the `count` will hold the length of the longest chain.

## How to Use

1. Include the necessary C++ libraries:

```cpp
#include <iostream>
#include <vector>
#include <algorithm>
```

2. Define the `Solution` class with the `findLongestChain` method, implementing the solution approach.

3. Inside the `main` function, create an instance of the `Solution` class.

4. Define the pairs of values as a vector of vectors:

```cpp
std::vector<std::vector<int>> pairs = {{1, 2}, {2, 3}, {3, 4}};
```

5. Call the `findLongestChain` method on the `Solution` instance, passing the pairs as an argument:

```cpp
int result = solution.findLongestChain(pairs);
```

6. Print the result:

```cpp
std::cout << "Length of the longest chain: " << result << std::endl;
```

## Complexity Analysis

- Time Complexity: O(n log n), where n is the number of pairs. Sorting the pairs takes O(n log n) time.
- Space Complexity: O(1), as no additional space is used other than the input and a few variables.

## Summary

The "Longest Chain of Pairs" problem is solved using a sorting-based approach and iterative checking. This solution provides an efficient way to find the length of the longest chain of pairs by sorting and iterating through the pairs, following a specific rule.
