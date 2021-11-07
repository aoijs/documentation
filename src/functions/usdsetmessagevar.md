---
description: Sets a variable value to the given message ID
---

# $setMessageVar

This function sets a value to the given message ID

```text
$setMessageVar[variable;value;message ID]
```

```javascript
bot.command({
name: "setMessageVar",
code: `Set the message var
$setMessageVar[reaction;5;780942849843396648]`
})
```

