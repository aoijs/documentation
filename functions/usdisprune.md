---
description: >-
  Used for Music Functions, whether or not the Client Message is being prune.
  (Returns true or false)
---

# $isPrune

#### Usage

```javascript
$isPrune
```

This function displays wether or not the queue message is pruned. Returns true or false.

#### Example

```javascript
bot.command({
    name: "isprune",
    code: `
    $isPrune
    `
})
```

