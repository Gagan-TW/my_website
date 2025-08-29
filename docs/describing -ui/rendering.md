---
title: Rendering UI in Refract
sidebar_label: Rendering UI
description: Understand how Refract enables rendering UI components with clarity, modularity, and efficiency using JSX.
---

# Rendering UI in Refract

Refract enables developers to build **reactive user interfaces** by combining the power of JSX with component-based architecture. This guide walks you through the core principles and patterns for rendering UIs effectively in Refract.

## What Does Rendering Mean?

Rendering is the process of displaying elements and components on the screen based on your application’s state and logic. In Refract, rendering UI is declarative—you describe **what** you want, and Refract handles **how** to update it.

---

## Basic JSX-Based Rendering

You can start rendering elements using simple JSX:

```jsx
function Welcome() {
  return <h1>Welcome to Refract!</h1>;
}
````

Refract components can return:

* Primitive HTML elements (`<div>`, `<p>`, etc.)
* Custom components
* Fragments (`<>...</>`)
* Conditional and list-rendered blocks

---

## Combining Logic with UI

Refract encourages rendering based on **application logic**:

```jsx
function Greeting({ isLoggedIn }) {
  return (
    <div>
      {isLoggedIn ? <p>Hello, User!</p> : <p>Please log in.</p>}
    </div>
  );
}
```

This declarative approach makes UIs predictable and maintainable.

---

## Rendering Nested Components

You can compose multiple components for modular UIs:

```jsx
function Header() {
  return <header>My App</header>;
}

function Content() {
  return <main>This is the content section.</main>;
}

function App() {
  return (
    <>
      <Header />
      <Content />
    </>
  );
}
```

---

## Conditional UI Rendering

Use `if` conditions or ternary operators to control what is shown:

```jsx
function Notification({ hasUnread }) {
  return (
    <div>
      {hasUnread && <span>You have unread messages</span>}
    </div>
  );
}
```

For more, see [Conditional Rendering](./conditional-rendering.md).

---

## Rendering Dynamic Lists

To display dynamic data (like user lists or items), use `map()`:

```jsx
const items = ['Lens', 'Optics', 'Refractions'];

function ItemList() {
  return (
    <ul>
      {items.map((item, idx) => (
        <li key={idx}>{item}</li>
      ))}
    </ul>
  );
}
```

For detailed explanation, refer to [Rendering Lists](./rendering-lists.md).

---

## Keeping UI Organized

Organize your UI into:

* **Atomic Components**: Buttons, Inputs
* **Composed Views**: Forms, Cards
* **Page Layouts**: Header, Footer, Main Content

This modularity promotes reuse and simplifies testing.

---

## Summary

* Rendering in Refract uses JSX and is fully reactive.
* Components can render primitives, custom UIs, and logic-driven blocks.
* Keep UI components small, focused, and reusable.
* Use state and props to drive UI changes.


