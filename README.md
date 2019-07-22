# Sorting Algorithm in Python

A sorting algorithm is an algorithm that puts elements of an array in a certain order.

### Features:
- In place: strictly an in-place sort algorithm needs only O(1) memory beyond the items being sorted.(no needs for extra memory)

- Recursive: some sorting algorithm are implemented in a recursive manner.(Dive and Conquer)

- Stable: stable sorting algorithms maintain the relative order of records with equal values.

### Lower Bound

For sorting N items we have to make Log(N!) comparisons. With stringling formula it can be reduced to N log(N).
- N log(N) time complexity is the lower bound for comparison based sorting algorithms.

- We can achieve O(N) running time as far as sorting is concerned with non comparison based algorithms.(Bucket Sort or Radix Sort)

## Bubble Sort

Repeatedly steps through the list to be sorted, compare each pair of adjacent items and swaps them if they are in the wrong order.

__Time Complexity : O(N^2)__

Bubble Sort has worst-case and average complexity both O(N^2). It it not a practical sorting algorithm.

In-place algorithm.

## Merge Sort

Merge Sort is a divide and conquer algorithm that was invented by John Von Neumann in 1945.

- Comparison algorithm and stable sorting.

- Not in place algorithm.

- Merge sort is often the best choice for sorting a linked list.

__Time Complexity : N log(N)__

1 - Divide the array into two sub arrays recursively.

2 - Sort these sub arrays recursively with Merge Sort again.

3 - If there is only a single item left in the sub array, we consider it to be sorted by definition.

4 - Merge the sub array to get the final sorted array.

- Often implement recursively.

## Quick Sort

- Quick Sort is an efficient sorting algorithm.

- It is a divide and conquer algorithm.

- Often implement recursively.

-  It is still a commonly used algorithm for sorting.

When implemented well, it can be about two or three times faster than its main competitors, Merge Sort and Heap Sort.

It was developed by Tony Hoare in 1959.

__Time Complexity : N log(N)__

Not Stable. Does not keep the relative order of items with equal value.

In place, does not need any additional memory.

Quick Sort gained widespread adoption, appearing, for example, in Unix as the default library sort subroutine. Hence, it lent its name to the C standard library subroutine qsort and in the reference implementation of Java.

## Selection sort

The algorithm divides the input list into two parts:
  - The sub-array of items already sorted.
  - The sub-array of items remaining to be sorted that occupy the rest of the array.

The algorithm proceeds by finding the smallest element in the unsorted sub-array.

It is an in place algorithm. (no need for extra memory)

Does not preserve the order of keys with equal values. (Not a stable sort)

__Time Complexity : O(N^2)__

## Radix Sort

Radix sort is an integer sorting algorithm that sorts data with integer keys by grouping the keys by individual digits that share the same significant position and value (place value)

- Radix Sort has two variants :
  - MSD : Most Significant Digit
  - LSD : Least Significant Digit
- Numbers are bucketed based on the value of digits moving left to right for MSD or
right to left from LSD.
- Radix Sort is a non-comparison sort.

#### Most Significant Digit - MSD

Radix Sort works by processing an integer or integer representation starting from the greatest digit, and moving towards the least significant digit. This method is usually solved by recursion.

#### Least Significant Digit - LSD

Radix Sort works by processing the least significant (smallest) digit first, and moving towards the greater, move significant digit as it continue to sort. This method is usually solved iteratively, using counting sort or bucket sort internally.


__Time Complexity : O(N)__

Pseudo Code :
  - Takes numbers in an input list.
  - Passes through each digit in those numbers, from least to most significant.
  - Looks at the values of those digits.
  - Buckets the input list according to those digits.
  - Renders the results from that bucketing.
  - Repeats this process until the list is sorted.

## Counting Sort

Counting sort is an efficient algorithm for sorting an array of positive integer. It is an integer sorting algorithm.

The ability to perform integer arithmetic on the keys allows integer sorting algorithms to be faster than comparison sorting algorithms in many cases.

Counting sort is an integer sorting algorithm. Values must be integers.

Counting sort is not a comparison based sorting algorithm, so linearithmic running time can be reduced.



It operates by counting the number of occurrences of each digit in the input array.

__Time Complexity : O(N + K)__

N : number of items we want to sort.
K : difference between the maximum and minimum values.

Only suitable if the variation in keys is not significantly greater than the number of items.
