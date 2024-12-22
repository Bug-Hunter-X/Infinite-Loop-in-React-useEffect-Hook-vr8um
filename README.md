# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications where an infinite loop occurs within a `useEffect` hook. The bug stems from incorrectly updating the state within the `useEffect`'s callback function, leading to a continuous re-render and subsequent state updates.

## Bug Description
The `MyComponent` component uses the `useState` hook to manage a count value. The `useEffect` hook is used with an empty dependency array (`[]`), intending to run only once after the component mounts. However, inside the `useEffect`, the `setCount` function is called to increment the `count`, causing the component to re-render continuously, leading to an infinite loop.

## Bug Solution
The solution involves restructuring the `useEffect` logic. Instead of directly updating the state within the `useEffect`, we can use a conditional statement or alternative methods to avoid the infinite loop. The solution provided avoids directly updating the state within the useEffect.