---
title: Optics
sidebar_label: Optics
description: Learn how optics in Refract enable focused, immutable access to application state.
slug: /reusing-logic/optics
---

# Optics in Refract

In Refract, **optics** are a powerful abstraction for working with deeply nested or complex application state. They allow you to _focus_, _view_, and _update_ specific parts of the state without mutating the whole object.

Optics make it easier to:
- Isolate specific fields in the state tree
- Compose access paths for deeply nested objects
- Perform updates immutably
- Improve modularity and reusability


## What Are Optics?

An optic represents a way to focus on part of a data structure. Refract primarily supports **lenses**, but it also uses ideas similar to **prisms** and **traversals**.

Example: creating a composed lens path.

```js
const userLens = lensProp('user');
const nameLens = lensProp('name');
const userNameLens = compose(userLens, nameLens);
````


## Viewing State

To read data with optics:

```js
const state = { user: { name: 'Gagan', age: 30 } };
const name = view(userNameLens, state); // Output: 'Gagan'
```

## Updating State

To immutably update data:

```js
const updatedState = set(userNameLens, 'Deep', state);
// Output: { user: { name: 'Deep', age: 30 } }
```

This operation does not mutate the original object.


## Example in a Component

```jsx
function UpdateName({ state, setState }) {
  const nameLens = compose(lensProp('user'), lensProp('name'));
  const name = view(nameLens, state);

  const update = () => {
    const newName = prompt('New name:', name);
    if (newName) {
      setState(set(nameLens, newName, state));
    }
  };

  return <button onClick={update}>Change Name</button>;
}
```


## Benefits

✅ Encourages functional programming
✅ Avoids boilerplate code
✅ Improves composability and reusability
✅ Works well with React state management

