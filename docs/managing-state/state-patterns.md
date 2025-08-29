---
title: Common State Patterns
description: Explore reusable and scalable state management patterns in Refract.
---

# Common State Patterns

Refract supports flexible design patterns for scalable state management.

## Pattern 1: Co-located State

Keep state local to components where it is only used there.

```js
const counter = useRefract({ count: 0 });
```
### Pattern 2: Global Shared State

Use Refract's context-like structure for app-wide state.
```
export const AppState = createRefractRoot({ theme: 'light', auth: {} });
```
### Pattern 3: Derived State Composition
```
Use refractions to maintain consistency across related pieces of state.
```
### Pattern 4: Custom Hooks
Encapsulate reusable logic using custom Refract hooks.
```
function useAuth() {
  const auth = useLens(AppState, 'auth');
  return { isLoggedIn: auth.value.token !== null };
}
```
### Recommendation
Choose patterns based on the scope, complexity, and lifecycle of the state.

