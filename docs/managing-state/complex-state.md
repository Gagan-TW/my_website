---
title: Complex State Management
description: Learn how to manage deeply nested and interrelated state structures in Refract.
---

# Complex State Management

In real-world applications, state often isn't flat or simple. You may need to manage deeply nested objects or multiple interdependent variables. Refract offers a structured approach to handling such complexities using optics like lenses and refractions.

## Challenges of Complex State

- Nested state objects increase cognitive load.
- Direct mutations cause unwanted side effects.
- Keeping derived state in sync becomes hard.

## Refract’s Approach

Refract encourages breaking state into manageable, reactive pieces through optics. This ensures:

- Localized updates using lenses.
- Predictable side effects.
- Scalable state logic.

## Example

```js
const state = useRefract({
  user: {
    name: '',
    address: {
      city: '',
      zip: ''
    }
  }
});

const userCity = useLens(state, 'user.address.city');
```
### Best Practices
- Avoid deeply nested state if unnecessary.
- Create custom optics for repeated access patterns.
- Use state slices where possible.
