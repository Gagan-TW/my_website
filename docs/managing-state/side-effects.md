---
title: Managing Side Effects
description: Learn to manage async operations and effects in Refract.
---

# Managing Side Effects

Refract integrates a structured pattern for handling side effects, ensuring they are controlled and traceable.

## Types of Side Effects

- API calls
- Timers
- Logging
- Navigation

## Best Practices

- Keep logic separate from state mutations.
- Use `useEffect` in combination with Refract hooks.
- Handle cleanup inside effect functions.

## Example

```js
useEffect(() => {
  fetchData().then(data => {
    state.data.set(data);
  });
}, []);
```
### Handling Async Logic
For async operations, avoid mutating state directly in the async function. Always ensure the state is updated safely inside the promise resolution block.
