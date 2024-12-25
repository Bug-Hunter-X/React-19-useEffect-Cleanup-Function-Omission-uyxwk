# React 19 useEffect Cleanup Function
This example demonstrates a common error in React 19's `useEffect` hook: omitting the cleanup function.  When an effect doesn't have a return function, it can lead to memory leaks, especially if it involves timers, subscriptions, or event listeners. The bug.js file showcases the problem, while bugSolution.js provides the corrected code.

## Bug
The `useEffect` hook in `bug.js` lacks a return function to properly clean up after the component unmounts. This results in the console log persistently triggering every time the component mounts, even after being removed from the DOM.