---
title: createComponent
sidebar_label: createComponent
sidebar_position: 1
---

# createComponent
The `createComponent` function lets you create a reusable UI block, also called a component.
## Why use it?
You can use `createComponent` to define how a part of your UI looks and behaves. This helps you organize your code and reuse it across your app.
## Example
```js
const MyComponent = createComponent(() => {
  return <div>Hello, user!</div>;
});
```
This example shows a basic component that displays “Hello, user!”
## When to use
Use createComponent when:
- You need to define a new part of your user interface.
- You want to reuse the same UI in different places.