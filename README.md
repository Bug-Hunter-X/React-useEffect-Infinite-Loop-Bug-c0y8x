# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite loop due to a missing dependency in the `useEffect` hook's dependency array.

## Bug Description

The `MyComponent` function uses the `useState` hook to manage a count.  The `useEffect` hook is intended to log the count to the console whenever it changes. However, because `count` is not included in the dependency array, the effect runs after every render, causing an infinite loop of re-renders and log messages.

## Solution

The solution involves correctly specifying the dependencies in the `useEffect` hook's dependency array. By including `count` in the dependency array, the effect only runs when the `count` value changes.