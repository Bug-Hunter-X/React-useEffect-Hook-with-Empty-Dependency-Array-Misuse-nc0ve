# React useEffect Hook with Empty Dependency Array Misuse

This repository demonstrates a common misuse of the React `useEffect` hook where an empty dependency array `[]` is used incorrectly, leading to unexpected behavior.  The example shows a counter component where the `useEffect` hook logs a message on every render, even though it should ideally only run once after the initial mount.  The solution demonstrates the correct usage of dependency arrays to trigger the effect only when specific values change.

## Bug

The bug lies in the `useEffect` hook's dependency array.  An empty array `[]` indicates that the effect should run only once after the initial render and not on subsequent state updates. However, due to a misunderstanding, the code will produce unwanted behavior. 

## Solution

The solution shows how to correctly specify the dependency array to achieve the intended functionality.  By including `count` in the array, the effect will only run whenever `count` changes. 