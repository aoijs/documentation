---
description: Sets a variable value to the current or given channel
---

# $setChannelVar

This function sets a value to the current/specified channel

```text
$setChannelVar[variable;value;channel ID (optional)]
```

```javascript
bot.command({
name: "setChannelVar",
code: `Set the channel var!
$setChannelVar[messageCount;12]`
})
```

