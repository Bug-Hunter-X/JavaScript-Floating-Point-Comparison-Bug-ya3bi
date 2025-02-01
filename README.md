# JavaScript Floating-Point Comparison Bug

This repository demonstrates a common error in JavaScript when comparing floating-point numbers for equality using the strict equality operator (===).

## The Problem

The `foo` function in `bug.js` attempts to check if two numbers are equal. However, due to the imprecision of floating-point representation, this comparison can be unreliable.  For example, `0.1 + 0.2` does not exactly equal `0.3` in JavaScript.

## The Solution

The `bugSolution.js` file provides a solution that addresses this issue using a tolerance-based comparison.  Instead of checking for strict equality, it checks if the absolute difference between the two numbers is less than a specified tolerance.