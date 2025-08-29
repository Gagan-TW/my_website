---
title: JSX in Refract
sidebar_label: JSX in Refract
description: Learn how Refract uses JSX to build component-based user interfaces with clarity and control.
---

# JSX in Refract

Refract builds on top of React, so JSX is at the core of its component syntax. JSX (JavaScript XML) lets you write HTML-like structures inside JavaScript, making UI code readable, expressive, and easy to maintain.

## What is JSX?

JSX stands for *JavaScript XML*. It is a syntax extension that looks like HTML but compiles to `React.createElement` calls.

```jsx
const greeting = <h1>Hello, world!</h1>;
````

This JSX is transformed into:

```js
const greeting = React.createElement('h1', null, 'Hello, world!');
```

## JSX in Refract Components

Since Refract is built with React at its core, all Refract components are written using JSX.

### Example: A Simple Refract Component

```jsx
function Welcome() {
  return (
    <div className="welcome-box">
      <h2>Welcome to Refract!</h2>
      <p>Build declarative UIs with the power of JSX.</p>
    </div>
  );
}
```

## Embedding Expressions

JSX supports embedding JavaScript expressions inside curly braces `{}`:

```jsx
const user = 'Gagandeep';
const element = <h1>Hello, {user}!</h1>;
```

## Conditional Rendering with JSX

Use conditional logic to render different elements:

```jsx
function Status({ isLoggedIn }) {
  return (
    <div>
      {isLoggedIn ? <p>You are logged in.</p> : <p>Please log in.</p>}
    </div>
  );
}
```

## Using JSX with Refract Lenses

You can combine JSX with Refract’s lens-based state management:

```jsx
import { useLens } from 'refract';
import { userLens } from '../lenses/userLens';

function Greeting() {
  const user = useLens(userLens);
  return <h1>Hello, {user.name}!</h1>;
}
```

## JSX Syntax Tips

* Use `className` instead of `class`.
* Use `htmlFor` instead of `for` in labels.
* Self-close void elements like `<img />` or `<input />`.

## Why JSX in Refract?

* **Declarative**: You describe what the UI should look like.
* **Composable**: Reuse components like functions.
* **Powerful**: Write JavaScript and markup together.

---

### Related Topics

* [Conditional Rendering](./conditional-rendering.md)
* [State Lenses](./lens.md)
* [Component Composition](../describing-ui/component-composition.md)

```



