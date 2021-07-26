---
description: >-
  Returns the position of <char> in <text>. Returns 0 if there's no char in
  text.
---

# $indexOf

This function returns the first matching position of the given character in the given text.

Raw usage: `$indexOf[text;character]` 

### Example Command: 

The example below returns `3` because the first `l` in `Hello` is at position 3.

```javascript
bot.command({
name: "index",
code: `
$indexOf[Hello;l]
`
})
```

