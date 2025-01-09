# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook.  The incorrect usage of `useEffect` without a dependency array causes an infinite render loop.

## Bug Description

The `useEffect` hook is used to perform side effects after every render.  If no dependency array (`[]`) is provided, the effect runs after every render, creating an infinite loop. This happens because the effect modifies the state, causing a re-render, which triggers the effect again, and so on.

## Bug Solution

The solution is to provide a dependency array to `useEffect`.  In this case, we only want the effect to run when `count` changes. Adding `[count]` as the dependency array resolves the issue.