---
title: Conditional Rendering
sidebar_label: Conditional Rendering
description: Learn how to show or hide UI elements in Refract based on dynamic conditions.
---

# Conditional Rendering

Conditional rendering is a common UI pattern that allows you to show or hide elements based on application state. In Refract, since it’s built on React, conditional rendering follows standard React principles—with enhanced clarity through state lenses.

## Basic Conditional Rendering

You can use standard JavaScript conditional statements inside your JSX.

```jsx
function Welcome({ isLoggedIn }) {
  return (
    <div>
      {isLoggedIn ? <h2>Welcome back!</h2> : <h2>Please log in.</h2>}
    </div>
  );
}
```

## Rendering Based on Refract State

When using Refract’s lens-based state, you can derive conditional UI from your focused data slices.

```jsx
import { useLens } from 'refract';
import { userLens } from '../lenses/userLens';

function Dashboard() {
  const user = useLens(userLens);

  return (
    <div>
      {user.isLoggedIn ? (
        <h2>Hello, {user.name}</h2>
      ) : (
        <h2>You need to log in</h2>
      )}
    </div>
  );
}
```

## Short-Circuit Rendering

Use logical `&&` to render elements only when the condition is true.

```jsx
{user.isAdmin && <AdminPanel />}
```

## Conditional CSS Classes

You can also apply classes conditionally:

```jsx
<button className={user.isLoggedIn ? 'btn-primary' : 'btn-disabled'}>
  Submit
</button>
```

## Best Practices

* Keep conditions concise for better readability.
* Move complex logic into variables before the return block.
* Avoid nested ternaries; use separate components instead.

---

