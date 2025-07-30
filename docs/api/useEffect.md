---
title: useEffect
sidebar_label: useEffect
sidebar_position: 3
---

# useEffect

The `useEffect` hook lets you run code when something changes, like when a component is shown or updated.

## Why use it?

Use `useEffect` to do things like:

- Load data from a server
- Set up timers
- Watch for changes in variables

## Example

```js
useEffect(() => {
  console.log('Component loaded');
}, []);
```
This runs once when the component is first shown.
## Another example
```
useEffect(() => {
  console.log('User ID changed');
}, [userId]);
```
This runs again only when `userId` changes.
## When to use
Use `useEffect` when you want your component to do something based on an update or event.
