# Sorting Algorithms

## Bubble Sort
Bubble Sort is a simple sorting algorithm that repeatedly steps through a list, compares adjacent elements, and swaps them if they are in the wrong order. The pass through the list is repeated until no swaps are needed, which indicates that the list is sorted.

### How Bubble Sort Works
1. Compare each pair of adjacent elements.
2. Swap them if they are in the wrong order.
3. Repeat the process for each element until no swaps are needed.

### Complexity
- **Time Complexity:** O(n^2) in the worst and average case
- **Space Complexity:** O(1)

## Selection Sort
Selection Sort is another simple sorting algorithm. It divides the input list into two parts: the sorted part and the unsorted part. In each iteration, the minimum element from the unsorted part is picked and moved to the end of the sorted part.

### How Selection Sort Works
1. Find the minimum element from the unsorted part of the list.
2. Swap it with the first unsorted element.
3. Move the boundary between the sorted and unsorted parts.
4. Repeat until the entire list is sorted.

### Complexity
- **Time Complexity:** O(n^2) in the worst and average case
- **Space Complexity:** O(1)

## Insertion Sort
Insertion Sort builds the sorted array one item at a time. It iterates through the input list, removing one element at a time and inserting it into its correct position in the sorted part of the array.

### How Insertion Sort Works
1. Start with the second element.
2. Compare it with the elements before it.
3. Shift all larger elements one position to the right.
4. Insert the current element into the correct position.
5. Repeat for each element in the list.

### Complexity
- **Time Complexity:** O(n^2) in the worst case; O(n) in the best case (when the list is already sorted)
- **Space Complexity:** O(1)

