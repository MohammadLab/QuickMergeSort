# Hybrid Merge-Quick Sort Algorithm

## Overview

The Hybrid Merge-Quick Sort is an innovative sorting algorithm that ingeniously combines the strengths of **Merge Sort** and **Quick Sort**. By leveraging Quick Sort's efficient partitioning technique and Merge Sort's robust merging strategy, this algorithm offers a unique approach to sorting arrays in C.

## Key Features

- **Innovative Hybrid Approach**
  - Utilizes Quick Sort's partitioning logic for array division
  - Employs Merge Sort's merging mechanism for combining sorted partitions
- **Recursive Divide-and-Conquer Design**
  - Breaks down sorting into smaller, manageable subproblems
- **Flexible Performance**
  - Competitive efficiency across various dataset characteristics

## Algorithm Workflow

1. **Partitioning Stage**
   - Divide the array using Quick Sort's partitioning method
   - Select a pivot (typically the last element in the current range)
   - Redistribute elements: smaller elements to the left, larger to the right

2. **Recursive Sorting**
   - Recursively apply the Hybrid Merge-Quick Sort to each partition
   - Continue dividing and sorting until base cases are reached

3. **Merging Stage**
   - Combine sorted partitions using Merge Sort's merging logic
   - Reconstruct the fully sorted array

## Core Functions

### `hybridMergeQuickSort(int arr[], int left, int right)`
- Recursively applies the Hybrid Merge-Quick Sort algorithm
- Manages sorting for the specified array segment

### `partition(int arr[], int left, int right)`
- Implements the partitioning logic
- Rearranges elements around a chosen pivot
- Returns the final pivot index

### `merge(int arr[], int left, int mid, int right)`
- Merges two sorted partitions back into the original array
- Ensures proper ordering of combined segments

### `printArray(int arr[], int size)`
- Utility function for displaying array contents

## Time Complexity Analysis

### Best Case: O(n log n)
- Pivot divides the array into perfectly balanced halves
- Recursion depth remains logarithmic
- Each recursion level processes entire array

### Average Case: O(n log n)
- Pivot creates reasonably balanced partitions
- Consistent performance across typical scenarios

### Worst Case: O(n²)
- Occurs with consistently unbalanced partitions
- Pivot selection results in highly skewed divisions
- Recursion depth becomes linear

## Space Complexity

- Merging step requires auxiliary arrays
- Additional space usage of O(n) at each recursion level
- Total space complexity: O(n)

## Practical Applications

Ideal for scenarios where:
- Absolute stability is not critical
- In-place partitioning is preferred
- Efficient merging of sorted segments is advantageous

## Limitations

- More complex implementation compared to standard sorting algorithms
- Increased memory overhead
- Performance can vary based on input characteristics

## Usage Example

```c
int arr[] = {3, 6, 8, 10, 1, 2, 1};
hybridMergeQuickSort(arr, 0, sizeof(arr)/sizeof(arr[0]) - 1);
// Array is now sorted: 1, 1, 2, 3, 6, 8, 10
```

## Compilation and Execution

```bash
gcc hybrid_sort.c -o hybrid_sort
./hybrid_sort
```

## License

MIT License - Feel free to use, modify, and distribute!
