---
description: Resets global user variable values
---

# $resetGlobalUserVar

This function resets everyones global user variable values to defaut value

```text
$resetGlobalUserVar[variable name]
```

```javascript
bot.command({
name: "resetglobaluservar",
code: `Resetted everyones money
$resetGlobalUserVar[money]`
})
```

