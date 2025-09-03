---
slug: why-optics-matter-in-refract
title: Why Optics Matter in Refract
authors:
  name: Gagandeep Kaur
  title: Technical Writer
tags: [refract, optics]
description: Discover how optics simplify state management in Refract.
date: 2025-08-29
---

When building user interfaces in JavaScript, managing state across components can be frustrating—especially when your application grows in complexity. That’s where **Refract** enters the scene with a game-changing abstraction: **optics**.

## 🔍 What Are Optics?

In Refract, *optics* are composable tools—like **lenses** and **refractions**—that help you read from and write to nested state structures in a clean, predictable way. Inspired by functional programming, optics allow you to focus only on the slice of state you care about.

Think of optics as a camera lens for your state—you choose exactly what part of the state tree to look at or update, without mutating the entire object.

```js
const userLens = lens(['user', 'profile']);
const userName = view(userLens, appState);
```

No more prop drilling or overuse of `useContext`.


## Why Optics Are Better Than Traditional State Management

Traditional frameworks often rely on reducers, state lifting, or context propagation. These work—but can get bloated fast.

**Refract offers:**

* ✅ Focused state updates with minimal re-renders
* ✅ Greater reuse of logic via optics composition
* ✅ Clear separation of data access and rendering
* ✅ A declarative style for modeling your app

## ✨ Optics in Action

Imagine you’re working on a form. With Refract, you don’t pass callbacks 5 levels deep. Instead, use a **lens** to bind your input directly to the right part of the state.

```jsx
<Input
  value={view(userLens, state)}
  onChange={(val) => update(userLens, val)}
/>
```

Clean. Predictable. Reusable.

## 🧠 Final Thoughts

Refract doesn't just give you another way to write components—it introduces a new mental model.

By embracing optics, you can *compose your UI and state logic like pure functions*, without the tangled mess of boilerplate and hacks.

Give it a try. You may never go back.

*Stay tuned for more posts in the Refract series!*


