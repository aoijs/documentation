---
description: Sets a global user var value
---

# $setGlobalUserVar

This function sets a value to a user. The value will remain the same throughout all guilds but will remain assigned to 1 user

```text
$setGlobalUserVar[variable;value;user ID (optional)]
```

```javascript
bot.command({
name: "setGlobalUserVar",
code: `Set your variable value to 4
$setGlobalUserVar[money;4]`
})
```

