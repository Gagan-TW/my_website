---
title: State with Refractions
description: Use refractions to compute derived state automatically.
---

# State with Refractions

Refractions are derived values that automatically recompute when underlying state changes.

## What is a Refraction?

A refraction is similar to a computed value. It reflects state transformations and updates automatically.

## Benefits

- Automatic recalculations.
- Readable and declarative.
- Zero boilerplate for derived values.

## Example

```js
const state = useRefract({ count: 2 });
const doubled = useRefraction(state, s => s.count * 2);
```
### When to Use
- To derive values from primitive state.
- To sync calculated values with UI.
- To reduce redundant logic in components.