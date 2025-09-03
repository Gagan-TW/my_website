---
title: Custom Optics
sidebar_label: Custom Optics
description: Define and compose your own optics for reusable state logic in Refract.
slug: /reusing-logic/custom-optics
---

# Creating Custom Optics in Refract

Refract allows you to create **custom optics**—reusable functions that simplify access to specific parts of your application state. These can help you avoid repetitive lens composition and encapsulate logic specific to your app.


## Why Create Custom Optics?

Custom optics are useful when:
- You frequently access the same nested field
- You want to abstract state paths behind meaningful names
- You need cleaner and more maintainable state logic


## Basic Custom Lens

You can export a lens from a utility file:

```js
// optics/userOptics.js

import { lensProp, compose } from 'refract-lens';

export const userLens = lensProp('user');
export const userNameLens = compose(userLens, lensProp('name'));
export const userAgeLens = compose(userLens, lensProp('age'));
````


## Using Custom Optics in a Component

```jsx
import { view, set } from 'refract-lens';
import { userNameLens } from '../optics/userOptics';

function UserNameDisplay({ state }) {
  const name = view(userNameLens, state);
  return <div>User Name: {name}</div>;
}
```

## Editable Example

```jsx
function UserEditor({ state, setState }) {
  const updateName = () => {
    const newName = prompt('Enter new name');
    if (newName) {
      setState(set(userNameLens, newName, state));
    }
  };

  return <button onClick={updateName}>Edit Name</button>;
}
```


## Composing Deeper Paths

You can combine optics deeply:

```js
const postsLens = lensProp('posts');
const firstPostTitleLens = compose(postsLens, lensIndex(0), lensProp('title'));
```

This reads and updates the title of the first post in an array immutably.


## Best Practices

* Keep your custom optics in a separate file like `optics.js` or `lenses.js`
* Use meaningful names (`userNameLens`, `settingsThemeLens`, etc.)
* Avoid hardcoding paths in components; use optics instead








