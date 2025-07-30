---
title: Refractions
description: Understand what refractions are and when to use them.
sidebar_position: 1
---

# Refractions

**Refractions** help your app do things like calling an API or waiting for a timer. These are called "side effects"—things that happen outside your app’s normal data flow.

Refract gives you a simple way to manage these side effects so your code stays clean and easy to understand.

## When to use refractions

Use refractions when your app needs to:
- Get data from an API
- Wait for a timer or delay
- Listen for events, like when a user clicks outside a component

## Example

```js
const user = useRefraction(fetchUserData, [userId]);
```
This code gets user data from an API. It runs again when `userId` changes.