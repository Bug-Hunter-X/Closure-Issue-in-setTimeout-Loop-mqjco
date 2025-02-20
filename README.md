# Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript closure issue that arises when using `setTimeout` within a loop.  The problem is that the closures created by `setTimeout` do not capture the value of `i` at the time of their creation, but rather capture a reference to the variable `i`. As a result, by the time `setTimeout` finally executes, the loop has already completed, and `i` has its final value of 10. 

The solution uses an immediately invoked function expression (IIFE) or `let` to ensure each closure has its own copy of `i`.