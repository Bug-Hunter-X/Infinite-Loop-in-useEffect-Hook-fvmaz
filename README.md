# React 18 useEffect Hook Bug
This repository demonstrates a common bug in React 18 related to the `useEffect` hook.  The bug involves an infinite rendering loop caused by a missing dependency array in the `useEffect` hook.

## Bug Description
The provided code uses the `useEffect` hook without a dependency array. This means that the effect runs after every render, leading to an infinite loop. Each render updates the `count` state, triggering another render, and so on. The console will show the count increasing rapidly.

## Solution
The solution involves adding a dependency array to the `useEffect` hook. This array specifies which values the effect depends on.  Only when these values change will the effect re-run.

## How to reproduce the bug
1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the rapidly increasing count in your console.

## How to fix the bug
1. Replace the existing `useEffect` hook with the corrected version from `bugSolution.js`
2. Re-run `npm start`