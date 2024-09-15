- In computer programming, an array is a structure for storing and retrieving data. We often talk about an array as if it were a grid in space, with each cell storing one element of the data. For instance, if each element of the data were a number, we might visualize a “one-dimensional” array like a list:

- A three-dimensional array would be like a set of tables, perhaps stacked as though they were printed on separate pages. In NumPy, this idea is generalized to an arbitrary number of dimensions, and so the fundamental array class is called `ndarray`: it represents an “N-dimensional array”.

- Most NumPy arrays have some restrictions. For instance:

	- All elements of the array must be of the same type of data.
	    
	- Once created, the total size of the array can’t change.
	    
	- The shape must be “rectangular”, not “jagged”; e.g., each row of a two-dimensional array must have the same number of columns.
	    

- When these conditions are met, NumPy exploits these characteristics to make the array faster, more memory efficient, and more convenient to use than less restrictive data structures.

- For the remainder of this document, we will use the word “array” to refer to an instance of `ndarray`.