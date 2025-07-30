---
title: useFlash
sidebar_label: useFlash
sidebar_position: 4
---

# useFlash

The `useFlash` hook lets you send short messages to the user—for example, a success or error message.

These messages are usually called "flash messages" and appear for a few seconds before going away.

## Why use it?

Use `useFlash` when you want to:

- Show a quick message after an action, like “Saved!” or “Failed to load.”
- Tell the user something happened, without changing the whole page.

## Example

```js
const flash = useFlash();

function handleClick() {
  flash.success('Your changes have been saved.');
}
```
In this example, a green success message appears when the user clicks a button.
## Other types of messages
You can also show different kinds of flash messages:
```
flash.error('Something went wrong.');
flash.info('New update available.');
flash.warning('Check your input.');
```
Each type gives a different color or style based on the message.
## When to use
Use useFlash when:
- You want to give user feedback after an action.
- You don’t want to redirect or reload the page to show the result.
