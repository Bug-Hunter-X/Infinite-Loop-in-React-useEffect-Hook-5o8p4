# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: creating an infinite loop by incorrectly updating state within the dependency array.  The `bug.js` file contains the erroneous code, while `bugSolution.js` provides the corrected implementation.

## Bug Description
The original code attempts to increment a state variable (`count`) within the `useEffect` hook's callback.  Because this callback is executed repeatedly due to the empty dependency array (`[]`), it continuously updates the state, leading to an infinite render loop.

## Solution
The corrected version avoids the infinite loop by using a functional update or refactoring the logic to update the state only under specific conditions.