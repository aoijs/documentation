---
description: Disables all role mentions in the bot's message.
---

# $disableRoleMentions

This function disables the mentions of a role in the user's message and sends it without pinging the role. Roles will be shown as the string but without a ping.

#### Usage

```javascript
bot.command({
name: "say", 
code: `$message
$disableRoleMentions` 
})
```

