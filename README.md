# Programming Assignment 2: Lexical Scoping

This repository contains the solution to the Coursera R Programming course's Programming Assignment 2 – Lexical Scoping, offered by Johns Hopkins University.

## 🧠 Objective

Implement two R functions to demonstrate the concept of lexical scoping and caching:
- `makeCacheMatrix()`: Creates a special matrix object that can cache its inverse.
- `cacheSolve()`: Computes or retrieves the cached inverse of the matrix.

## 📁 Files

- `makeCacheMatrix.R` – Contains the function to create a cache-enabled matrix.
- `cacheSolve.R` – Contains the function that computes or retrieves the inverse.

## 🧪 How to Test

```r
source("makeCacheMatrix.R")
source("cacheSolve.R")

m <- matrix(c(2, 2, 1, 4), 2, 2)
cm <- makeCacheMatrix(m)

# First call: calculates and caches the inverse
cacheSolve(cm)

# Second call: retrieves from cache
cacheSolve(cm)
