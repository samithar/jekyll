---
title:  malloc in FreeRTOS (or Any)
header:
  teaser: 
categories: 
  - Programming
tags:
  - C
---

# malloc(size_t size)

`malloc`([1]) is a C standard library function that allocates a a block of memory (size in bytes), and returns a pointer to the beginning of that memory block. The contents of the memory block is not initialized hence remaining with intermediate/undefined values. This function returns a `NULL` if there is no memory to be allocated, i.e. if the request fails. Under this scenario, dereferencing is not a permitted operation. `malloc` plays a vital part in embedded systems, as they are, still, considered as low resource (memory).

## malloc example

``` C
int *ptr_one;
ptr_one = (int *)malloc(sizeof(int));
if (ptr_one == 0) //if malloc failed (returns a null pointer)
	{
	printf("ERROR: Out of memory\n");
	return 1;
	}

```

The above code initializes an integer pointer, and allocates the `sizeof(int)`. Remember, since malloc retuns a general purpose pointer,
in which, in `C` we call as a `void pointer` it needs to be casted to whatever the type we require. 

When you allocate the memory, and be done with it, you must `free` that particular block of memory back to the system.

## In FreeRTOS?
FreeRTOS has its own memory management schemes, in particular that is what you specify with the heapX.c file, in which X corresponds to the implemented mechanism. Listed as follows ([2]).

heap_1 - the very simplest, does not permit memory to be freed
heap_2 - permits memory to be freed, but not does coalescence adjacent free blocks.
heap_3 - simply wraps the standard malloc() and free() for thread safety
heap_4 - coalescences adjacent free blocks to avoid fragmentation. Includes absolute address placement option
heap_5 - as per heap_4, with the ability to span the heap across multiple non-adjacent memory areas

## so what?

So, FreeRTOS has its own memory usage

## Solution
[1]:http://man7.org/linux/man-pages/man3/realloc.3.html
[2]:https://www.freertos.org/a00111.html

