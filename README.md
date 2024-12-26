# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug causes an infinite loop due to a missing dependency in the effect's dependency array.

## Bug Description

The `MyComponent` function uses `useEffect` to log the current count. However, because `count` is not included in the dependency array, the effect runs on every render, causing `setCount` to be called continuously, leading to an infinite loop.

## Bug Solution

The solution involves adding `count` to the dependency array. This ensures the effect only runs when `count` changes.

## How to reproduce

1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the infinite loop in the console.
5. Uncomment the corrected code in `bugSolution.js` to see the fix.
