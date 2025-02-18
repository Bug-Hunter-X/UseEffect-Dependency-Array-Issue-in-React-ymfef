# React useEffect Dependency Array Issue

This repository demonstrates a common error related to the dependency array in React's `useEffect` hook.  The provided `bug.js` file showcases an example where the effect runs on every render. The `bugSolution.js` provides the correct solution.

## Problem

The `useEffect` hook is often used to perform side effects after a component renders.  However, the dependency array is crucial in controlling when the effect runs. An empty array `[]` indicates that the effect should only run once, after the initial render.  Failure to use an empty array correctly will lead to the effect running on every render, potentially causing performance issues or unexpected behavior.

## Solution

The solution involves ensuring that the dependency array correctly reflects the variables that the effect depends on.  If the effect should run only once, the dependency array should be empty `[]`.  If it depends on a state variable, include that variable in the array.