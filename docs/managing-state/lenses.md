---
title: Using Lenses
description: Understand how lenses help access and update nested state in Refract.
---

# Using Lenses
Lenses in Refract allow focused access to specific parts of your state. They act like "zoom lenses" for deeply nested objects.

## What is a Lens?
A lens is a functional abstraction that focuses on a part of a data structure.

## Why Use Lenses?
- Simplifies access to nested fields.
- Avoids direct mutation.
- Enables reactive updates.

## Basic Example
```js
const state = useRefract({ profile: { name: 'John' } });
const nameLens = useLens(state, 'profile.name');

nameLens.set('Jane'); // updates only name
```
### Lens Composition
Lenses can be composed to create reusable access patterns:

``` const cityLens = composeLens(userLens, 'address.city');
```
### Tip
Prefer using useLens over manual destructuring when accessing state reactively.


