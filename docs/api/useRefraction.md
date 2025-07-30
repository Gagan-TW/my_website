---
title: useRefraction
sidebar_label: useRefraction
sidebar_position: 2
---
# useRefraction
The `useRefraction` hook lets your component respond to changes in the state or data it depends on.
## Why use it?
This hook helps your component stay updated when something it relies on changes, like a user's selection or input.
## Example
```js
const user = useRefraction(state => state.user);
```
This code gets the latest user value from the shared state.

## When to use
Use `useRefraction` when:
- Your component depends on a shared or global state.
- You want your component to re-render when specific values change.