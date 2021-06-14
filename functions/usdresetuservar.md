---
description: Resets everyones variable value for the server
---

# $resetUserVar

This function resets everyone's user variable values to default value in the current guild

```javascript
$resetUserVar[variable]
```

```javascript
bot.command({
name: "resetuservar",
code: `Resetted everyones money
$resetUserVar[money]`
})
```

