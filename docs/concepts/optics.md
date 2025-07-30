---
title: Optics
description: Use optics to work with complex or nested data.
sidebar_position: 3
---

# Optics

**Optics** help you work with data that has many levels or parts. For example, if your data looks like a tree or a list inside another list, optics make it easier to find and update the part you want.

Optics build on lenses and let you go deeper into your data without writing a lot of code.

## Why use optics

Optics help you:
- Work with deeply nested data
- Keep your code simple and readable
- Avoid errors when parts of the data are missing

## Example

```js
const email = user.optic().focus('contact').focus('email');
```
This finds the email address inside a contact object. If the contact object is missing, Refract handles it safely.

