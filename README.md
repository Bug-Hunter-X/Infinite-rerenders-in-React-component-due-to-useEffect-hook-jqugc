# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug causes infinite rerenders, leading to performance issues and potentially crashing the application.

## Bug Description

The `useEffect` hook is designed to perform side effects after every render. However, if the dependency array is missing or incorrect, it can lead to an infinite loop. In this case, the effect function logs the count to the console and updates the state, causing the component to re-render and execute the effect again repeatedly. 

## How to Reproduce

Clone the repository and run the React application.

## Solution

The solution involves correctly specifying the dependency array in the `useEffect` hook. By including `count` in the array, the effect only runs when the value of `count` changes, preventing the infinite loop.