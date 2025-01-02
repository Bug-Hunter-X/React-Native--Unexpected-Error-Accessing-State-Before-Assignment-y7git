# React Native: Unexpected Error Accessing State Before Assignment

This repository demonstrates a common error in React Native applications: accessing state variables or props before they've been assigned a value.  This often occurs when dealing with asynchronous operations. The `bug.js` file shows the problematic code, while `bugSolution.js` offers a corrected implementation.

## Problem

Attempting to access `data.name` before the asynchronous `fetch` call completes results in an error because `data` is initially `null`. 

## Solution

The solution involves checking if `data` is defined before accessing its properties. Using optional chaining (`?.`) and nullish coalescing (`??`) provides a concise and safe way to handle this.