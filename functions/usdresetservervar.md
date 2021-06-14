---
description: Resets a server variable value
---

# $resetServerVar

This function resets the variable to default value for the current guild

```text
$resetServerVar[variable]
```

```javascript
bot.command({
name: "resetservervar",
code: `Resetted server xp
$resetServerVar[serverxp]`
})
```

