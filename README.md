# React useEffect setInterval Memory Leak

This example demonstrates a common mistake in React: using `setInterval` within a `useEffect` hook without a cleanup function. This leads to a memory leak because the interval continues indefinitely, even after the component unmounts.  The solution shows how to properly use `setInterval` with `useEffect` by returning a cleanup function.

## Bug:
The bug is present in `bug.js`.  The `setInterval` function is used without the necessary cleanup to prevent memory leaks when the component is unmounted.