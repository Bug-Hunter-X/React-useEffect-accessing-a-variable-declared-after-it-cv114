# React useEffect Variable Scope Issue

This repository demonstrates a common error in React when using the `useEffect` hook: attempting to access a variable declared *after* the `useEffect` call within the same component. This results in the variable being `undefined` because the variable's declaration is executed after the useEffect callback. 

## Bug

The `bug.js` file contains the erroneous code. The `useEffect` hook attempts to access the `myVar` variable, but because `myVar` is declared after the `useEffect` is defined and executed during initial render, it is `undefined` when the `useEffect` runs causing error or unexpected behavior. 

## Solution

The `bugSolution.js` file provides a corrected version. The solution involves moving the variable declaration `myVar` to above the `useEffect` hook or by using `useRef` to directly access the value avoiding the timing issue.