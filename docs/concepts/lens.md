---
title: Lenses
description: Learn how to focus on small parts of your data using lenses.
sidebar_position: 2
---

# Lenses

A **lens** is a tool that helps you work with just one small part of your app’s data. You don’t have to update the entire state—just the part you need.

Think of it like a zoom lens on a camera. It helps you see and change a small detail clearly without touching everything else.

## Why use lenses

Lenses help you:
- Change part of your data without breaking other parts
- Keep your code short and clear
- Use the same logic in different places

## Example

```js
const name = useLens(user, 'name');
```
This gives you just the user's name from the `user` data. You can update it directly.
