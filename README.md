# React useEffect Infinite Loop

This repository demonstrates a common React bug involving the `useEffect` hook and how to fix it.

The `bug.js` file contains code that creates an infinite loop due to a missing dependency array in `useEffect`.  The `bugSolution.js` file shows the corrected code.

## Bug

The `useEffect` hook in `bug.js` runs after every render, because it's missing a dependency array. This causes an infinite loop because updating the count triggers a re-render, which triggers the `useEffect` again.

## Solution

The `bugSolution.js` demonstrates the correct way to use `useEffect`.  By including `[count]` as the dependency array, the `useEffect` only runs when the `count` value changes.