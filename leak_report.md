# Leak report

The sole memory leak I found was in the strip function, when it allocates the memory for the result array it fails to free the memory before it finishes. One could fix this (and I will fix this, after I finish writing this report) by simply freeing the memory address calloc'd in that function within the main function. 

