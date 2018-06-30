---
title:  malloc in FreeRTOS (or Any)
header:
  teaser: 
categories: 
  - Programming
tags:
  - C
---

malloc(size_t size)

`malloc`([1]) is a C standard library function that allocates a a block of memory (size in bytes), and returns a pointer to the beginning of that memory block. The contents of the memory block is not initialized hence remaining with intermediate/undefined values. This function returns a `NULL` if there is no memory to be allocated, i.e. if the request fails. Under this scenario, dereferencing is not a permitted operation. `malloc` plays a vital part in embedded systems, as they are, still, considered as low resource (memory).



[1]:http://man7.org/linux/man-pages/man3/realloc.3.html


