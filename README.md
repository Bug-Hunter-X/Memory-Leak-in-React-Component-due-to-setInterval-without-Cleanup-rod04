# React setInterval Cleanup
This repository demonstrates a common error in React applications: using `setInterval` within `useEffect` without proper cleanup. This can lead to memory leaks and unexpected behavior.

## Bug
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it fails to provide a cleanup function to stop the interval when the component unmounts.  This results in the interval continuing to run indefinitely, even after the component is no longer rendered.  This will eventually lead to a memory leak.

## Solution
The `bugSolution.js` file demonstrates the correct way to use `setInterval` within `useEffect`. It includes a return statement within the `useEffect` hook that uses `clearInterval` to stop the interval when the component is unmounted or the effect is changed.  This prevents memory leaks and ensures clean behavior.

## How to run
1. Clone the repository.
2. Navigate to the repository's directory.
3. Run `npm install`.
4. Run `npm start`.