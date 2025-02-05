# React StrictMode Warning: useEffect Unnecessary Re-renders

This repository demonstrates a common React StrictMode warning related to the `useEffect` hook causing unnecessary re-renders.  The warning is triggered because the effect function runs on every state update, even when the dependencies haven't changed.  This can lead to performance issues and unexpected behavior.

## Problem

The `MyComponent` component uses `useEffect` to log a message whenever the `count` state changes. This is unnecessary and inefficient.  StrictMode highlights this inefficiency.

## Solution

The issue is resolved by ensuring the `useEffect` only runs when the actual dependencies change using dependency array for `useEffect`. 

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `npm start` to start the development server.
4. Open your browser and observe the console warnings in the browser's developer tools.