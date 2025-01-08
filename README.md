# Unnecessary Re-renders in React useEffect Hook

This example demonstrates a common mistake in using the React `useEffect` hook where the effect runs after every render, leading to unnecessary re-renders and potential performance degradation.  The solution shows how to optimize the `useEffect` hook to only run when the dependency `count` changes, preventing redundant executions.

## Bug
The `useEffect` hook in `bug.js` lacks an appropriate dependency array.  This causes the `console.log` statement to execute on every render, even if the value of `count` hasn't changed.  This can lead to performance problems in more complex applications.

## Solution
The `bugSolution.js` shows the corrected version.  By including `[count]` as the dependency array, the effect runs only when the value of `count` changes, optimizing its execution and improving efficiency.