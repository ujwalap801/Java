# Merge Sort

Merge sort is a sorting algorithm that follows the divide-and-conquer approach.

## How it works:
1. **Divide**: The input array is repeatedly divided into two halves until each subarray contains only one element.
2. **Conquer**: These single-element subarrays are considered sorted.
3. **Merge**: The sorted subarrays are merged pair-wise to form larger sorted subarrays until the entire array is sorted.

## Key characteristics:
- **Efficient**: It has a time complexity of O(n log n) in all cases.
- **Stable**: It preserves the relative order of equal elements.
- **Recursive**: It's implemented using recursion.
- **General-purpose**: Works well for various data types.


# Quick Sort

Quick sort is another efficient sorting algorithm that, like merge sort, employs the divide-and-conquer strategy. However, it operates differently.

## How it works:

1. **Pick a pivot**: An element from the array is chosen as the pivot.
2. **Partition**: The array is rearranged such that all elements smaller than the pivot come before it, and all greater elements come after.
3. **Recursion**: The same process is applied recursively to the sub-arrays on both sides of the pivot until the entire array is sorted.

## Key characteristics:

- **Efficient**: It has an average time complexity of O(n log n), but its worst-case time complexity is O(n^2).
- **In-place**: It sorts the array without requiring extra space.
- **Recursive**: It's implemented using recursion.
- **General-purpose**: Works well for various data types.
