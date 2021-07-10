---
description: Aliases allow users to run the same command using different triggers.
---

# Aliases

## Default Aliases

```javascript
bot.command({
name: "name",
aliases: ['name2','name3'],
code: `code`
})
```

*Aliases are listed in a [array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array).*

## Aliases for Command Handler

```javascript
module.exports = ({
name: "name",
aliases: ['name2','name3'],
code: `code`
})
```
