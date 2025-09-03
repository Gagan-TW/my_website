---
title: useOptic
sidebar_label: useOptic
sidebar_position: 5
---

# useOptic

The `useOptic` hook helps you focus on a small part of a bigger state or data object.

It's similar to a zoom tool—you can read or update just one field without affecting the whole thing.

## Why use it?

If your app has a lot of data, it’s easier to manage when you only work with the part you need. `useOptic` helps you do that safely and clearly.

## Example

```js
const name = useOptic(user).focus('name');
```
This gives access to the `name` field in the user object.

You can now read or change `name` directly:
```
name.set('Alice');
console.log(name.get()); // Alice
```
## When to use
Use `useOptic` when:

- You’re working with nested data like user.contact.email

- You only want to update one part of a big object

- You want to avoid unnecessary re-renders