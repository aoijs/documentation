---
description: Deletes the user message
---

# $deletecommand

This will deletes the user's message that triggered the command

#### Usage

```javascript
bot.command({
name: "command",
code: `hi
$deletecommand` //Will delete !command
})
```

