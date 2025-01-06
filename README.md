# TypeScript Type Guard Inconsistency with Optional Parameters

This repository demonstrates a subtle bug in TypeScript related to type guards and optional parameters.  The `greet` function correctly handles null values, but it fails when an undefined value is passed. This is because the type guard `if (name === null)` does not account for the possibility of `undefined`, leading to a runtime error.  The solution shows how to handle both null and undefined values correctly.

## How to Reproduce

1. Clone the repository.
2. Run `tsc bug.ts` to compile the code.
3. Run `node bug.js`. Observe the error.
4. Run `tsc bugSolution.ts` and `node bugSolution.js` to see the corrected behavior.