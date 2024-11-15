# Generic Sorting Algorithms Library

## _A Comprehensive Library of 17+ Sorting Algorithms for C and C++_

This is a generic data structure library built in C that supports sorting a variety of data types using 17+ different sorting algorithms. It is designed to work seamlessly with both C and C++ projects, offering developers flexibility and performance for their sorting needs.

- Written in C with support for C++
- Sort any type of data using custom comparator functions
- Comprehensive set of sorting algorithms

## Features

- Supports both primitive data types and user-defined structures.
- Easy-to-use comparator function for custom data sorting.
- Includes 17+ sorting algorithms:
  - Bubble Sort
  - Quick Sort
  - Merge Sort
  - Heap Sort
  - Radix Sort (for integers only)
  - and many more!

✨ Custom data type sorting with a function! ✨

## Tech

The library is built purely in C and can be linked in both C and C++ projects. It focuses on providing a clean and flexible API for sorting various data types with custom comparator functions.

- **C** and **C++** compatible
- Includes efficient implementations of classic algorithms
- Provides a flexible API with function pointers for custom sorting

## Supported Sorting Algorithms

This library includes the following sorting algorithms:

```c
//Bubble Sort
int bubbleSort(void *arr, size_t n, size_t elemSize, int (*compare)(void *, void *));

//Linear Sort
int linearSort(void *arr, size_t n, size_t elemSize, int (*compare)(void *, void *));

//Insertion Sort
int insertionSort(void *arr, size_t n, size_t elemSize, int (*compare)(void *, void *));

//Selection Sort
int selectionSort(void *arr, size_t n, size_t elemSize, int (*compare)(void *, void *));

//Shell Sort
int shellSort(void *arr, size_t n, size_t elemSize, int (*compare)(void *, void *));

//Quick Sort
void quickSort(void *arr, size_t left, size_t right, size_t elemSize, int (*compare)(void *, void *));

//Merge Sort
void mergeSort(void *arr, size_t left, size_t right, size_t elemSize, int (*compare)(void *, void *));

//Heap Sort
int heapSort(void *arr, size_t n, size_t elemSize, int (*compare)(void *, void *));

//Radix Sort (for integers)
int radixSort(int *arr, size_t n);

//Pancake Sort
int pancakeSort(void *arr, size_t n, size_t elemSize, int (*compare)(void *, void *));

//Gnome Sort
int gnomeSort(void *arr, size_t n, size_t elemSize, int (*compare)(void *, void *));

//Brick Sort
int brickSort(void *arr, size_t n, size_t elemSize, int (*compare)(void *, void *));

//Counting Sort (for positive integers)
int countingSort(int *arr, size_t n);

//Pigeonhole Sort (for integers)
int pigeonHoleSort(int *arr, size_t n);

//Stooge Sort
void stoogeSort(void *arr, size_t l, size_t r, size_t elemSize, int (*compare)(void *, void *));

//Tim Sort
int timSort(void *arr, size_t n, size_t elemSize, int (*compare)(void *, void *));

//Cocktail Shaker Sort
int cocktailShakerSort(void *arr, size_t n, size_t elemSize, int (*compare)(void *, void *));

//Binary Insertion Sort
int binaryInsertionSort(void *arr, size_t n, size_t elemSize, int (*compare)(void *, void *));

//Address Calculation Sort
int addressCalculationSort(void *arr, size_t n, size_t elemSize, int (*compare)(void *, void *));
```

### sort.h

The `sort.h` file includes function declarations for each of the sorting algorithms. Most functions require parameters for the array to be sorted, the element size, the number of elements, and a comparator function pointer to handle custom data structures.

Example function declaration:

```c
int bubbleSort(void *array, size_t n, size_t elemSize, int (*compare)(void *, void *));

```

### utils.h

The utils.h file provides additional utility functions that support the sorting algorithms:

- swap: Swaps two elements in memory.
- Queue Management: Includes a queue data structure with functions to initialize, add, remove, and check if a queue is empty.

Example:

```c
void initQueue(Queue *queue);
void addToQueue(Queue *queue, int value);
int removeFromQueue(Queue *queue);
int isQueueEmpty(Queue *queue);
```

## Installation

To use the library, simply clone the repository and include the header and source files in your project.

```sh
git clone https://github.com/iam-harshprajapat/Generic-Sorting-Algorithm-library-in-C-CPP.git'
```

Add the `.c` and `.h` files to your project and compile them along with your application.
Copy the include and src files into your project directory.
Compilation and Usage
To compile, link the source files with your main program:

```sh
gcc -o main main.c src/*.c -Iinclude
```

## Example Usage

Here's a detailed example demonstrating how to use the bubbleSort function in this library.

Parameters

```sh
array: Pointer to the array to be sorted.
n: Number of elements in the array.
elemSize: Size of each element (use sizeof(type)).
compare: A pointer to a comparator function that takes two void pointers and returns:
0 if the two elements are equal,
a negative value if the first element is smaller,
a positive value if the first element is larger.
```

Example Code

Code:

```c
#include "sort.h"
#include <stdio.h>
#include <stdlib.h>

// Comparator function for integers
int intComparator(void *a, void *b) {
    int x = *(int *)a;
    int y = *(int *)b;
    return x - y;
}

int main() {
    int arr[] = {5, 2, 9, 1, 5, 6};
    size_t n = sizeof(arr) / sizeof(arr[0]);

    // Sort the array using bubbleSort
    int result = bubbleSort(arr, n, sizeof(int), intComparator);

    // Check if sorting was successful
    if (result == SUCCESS) {
        printf("Sorted array: ");
        for (size_t i = 0; i < n; i++) {
            printf("%d ", arr[i]);
        }
    } else {
        printf("Sorting failed.");
    }

    return 0;
}
```

Explanation

Define a Comparator: The intComparator function compares two integers, returning the difference between them.
Call bubbleSort: Pass the array, its length, the size of each element, and the comparator to bubbleSort.
Check Result: Verify if sorting was successful by checking if bubbleSort returned SUCCESS.
Print Result: Print the sorted array if successful.

## Development

Want to contribute? Feel free to fork the repository and submit a pull request with your improvements. All contributions are welcome!

# Contact

##### Gmail: s.harshprajapat@gmail.com

##### LinkedIn: https://www.linkedin.com/in/harsh-prajapat-india/
