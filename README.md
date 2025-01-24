# Unexpected Behavior with Mutable Variables in F#

This example demonstrates a common pitfall in F# when working with mutable variables.  In the provided code, the `swap` function attempts to swap the values of `x` and `y`. However, because F# mutable variables are passed by reference, the changes made inside the `swap` function do not affect the original variables outside the scope of the function.

**The Problem:** The `swap` function modifies the local copies of `x` and `y` passed to it, leaving the original `x` and `y` unchanged.

**The Solution:** To correct the behavior, it's necessary to return the swapped values from the `swap` function and assign them back to `x` and `y`.

This repository includes two files:
- `bug.fs`: Shows the incorrect implementation.
- `bugSolution.fs`: Demonstrates the corrected implementation.