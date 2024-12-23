# React useEffect Hook Dependency Array Issue

This repository demonstrates a common issue with the React `useEffect` hook: unnecessary re-renders due to missing dependencies in the dependency array.  The `bug.js` file contains the problematic code.  The solution in `bugSolution.js` correctly adds the `count` variable to the dependency array, ensuring the effect only runs when the count changes.  This fixes performance issues caused by the infinite render loop.

## Problem:

The initial implementation causes the `useEffect` hook to run on every render.  This leads to performance degradation, especially in complex components.

## Solution:

Adding `count` to the dependency array ensures that the effect only runs when the `count` state variable changes.