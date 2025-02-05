# React useEffect Cleanup and setInterval Issue

This repository demonstrates a common React bug involving the `useEffect` hook and the `setInterval` function. The bug causes a memory leak due to a missing cleanup function in `useEffect` and an incorrect interval setup which may not work as expected.

## Bug Description
The `MyComponent` uses `useEffect` to set up an interval that increments a counter every second. However, it's missing a cleanup function to clear the interval when the component unmounts, causing a memory leak. Additionally, the way the `setInterval` is set up may lead to unexpected behavior or incorrect timing, as the function is recreated each render.