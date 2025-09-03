---
id: components
title: Creating and Nesting Components
---

# Creating and Nesting Components

In Refract, the user interface is built using **components**. Components are reusable, independent pieces of UI—like buttons, headers, cards, or even full pages.

Each component in Refract is defined using the `createComponent()` function and returns JSX-like syntax.


## What is a component?

A component is:

- A JavaScript function
- Registered with Refract using `createComponent()`
- Must start with a **capital letter**
- Returns JSX-like code (similar to HTML)


## Example: Your first component

```js
import { createComponent } from 'refract';

const MyButton = createComponent(() => {
  return <button>I'm a button</button>;
});
