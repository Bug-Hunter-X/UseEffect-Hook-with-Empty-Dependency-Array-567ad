# useEffect Hook with Empty Dependency Array

This repository demonstrates a common issue encountered when using the `useEffect` hook in React.  The issue is related to the behavior of the dependency array.

## Bug Description
The provided `MyComponent` uses `useEffect` with an empty dependency array (`[]`). This is typically used to perform side effects only once after the component's initial mount. However, if the intention was to run the effect after every render, the empty dependency array prevents this.

## Solution
To fix this, remove the empty dependency array.  This will cause the effect to run after every render. Note that this can lead to performance issues if not handled carefully.  Consider adding appropriate dependencies to the array to optimize the effect's execution.