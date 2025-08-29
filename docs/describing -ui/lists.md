---
title: Rendering Lists
sidebar_label: Rendering Lists
description: Learn how to render dynamic lists of components in Refract using JSX and array methods.
---

# Rendering Lists in Refract

Rendering lists is a common pattern in Refract when displaying dynamic collections of data—such as items, users, messages, or tasks. This guide explains how to use JSX to render lists efficiently and clearly.

## Basics of List Rendering

In Refract (which extends React), you can render lists using JavaScript's array `map()` function inside JSX.

### Example: Rendering a List of Items

```jsx
const fruits = ['Apple', 'Banana', 'Orange'];

function FruitList() {
  return (
    <ul>
      {fruits.map((fruit, index) => (
        <li key={index}>{fruit}</li>
      ))}
    </ul>
  );
}
````

**Explanation**:

* The `map()` method creates a new `<li>` element for each item.
* The `key` prop helps React/Refract identify each list item for efficient updates.

## Using Keys

The `key` prop must be unique among siblings. It helps in efficient re-rendering. Avoid using array indexes as keys when the list is dynamic.

### Better Example with Unique Keys

```jsx
const users = [
  { id: 101, name: 'Gagandeep' },
  { id: 102, name: 'Ankur' },
];

function UserList() {
  return (
    <ul>
      {users.map((user) => (
        <li key={user.id}>{user.name}</li>
      ))}
    </ul>
  );
}
```

## Conditional List Rendering

You can also conditionally render elements within the list.

```jsx
const tasks = [
  { id: 1, title: 'Write docs', completed: true },
  { id: 2, title: 'Review PR', completed: false },
];

function TaskList() {
  return (
    <ul>
      {tasks
        .filter((task) => !task.completed)
        .map((task) => (
          <li key={task.id}>{task.title}</li>
        ))}
    </ul>
  );
}
```

## Rendering Refract Components in a List

You can render full components in a list.

```jsx
function Task({ title }) {
  return <li>{title}</li>;
}

function TaskBoard({ tasks }) {
  return (
    <ul>
      {tasks.map((task) => (
        <Task key={task.id} title={task.title} />
      ))}
    </ul>
  );
}
```

## Summary

* Use `map()` to iterate and render arrays.
* Always provide a unique `key` prop.
* Lists can contain raw JSX or reusable components.
* Combine with filters or conditions for dynamic rendering.

---




