---
description: Checks if the bot has specified permissions
---

# $onlyBotPerms

This function only allows the command to be ran if the bot has the specified [permissions](../other/permissions.md)

```
$onlyBotPerms[perm1;perm2;...;error when no perms]
```

```javascript
bot.command({
name: "special",
code: `SpecialCommand
$onlyBotPerms[ban;;x: Bot doesn't have ban permissions]`
})
```
