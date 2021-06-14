---
description: Sets a server variable value
---

# $setServerVar

This function sets a value to a variable for the current/specified guild

```javascript
$setServerVar[variable;value;guild id (optional)]
```

```javascript
bot.command({
name: "setServerVar",
code: `Set a server var
$setServerVar[members;56]`
})
```

