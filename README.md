# F# Mutable Variable Swap Bug

This repository demonstrates a common issue in F# involving mutable variables and pass-by-value semantics.  When attempting to swap two mutable variables within a function, the original variables remain unchanged outside the function's scope. This is because F# passes mutable variables by value, creating copies instead of references.

The `bug.fs` file shows the erroneous code, while `bugSolution.fs` provides a corrected implementation.  The solution uses techniques to correctly modify the original variables either by passing them as mutable references or by returning a tuple.

## How to Reproduce

1. Clone the repository.
2. Open `bug.fs` and run the code. Observe that the original variables remain unchanged.
3. Then, open `bugSolution.fs` and observe the correct result.