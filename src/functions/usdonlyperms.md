---
description: Checks if user has specified perms
---

# $onlyPerms

This function only allows the command to be ran when a user has the specified [permissions](../guide/begin/permissions.md)

```text
$onlyPerms[perm1;perm2;...;error when user has no perms]
```

```javascript
bot.command({
name: "special",
code: `Special Command
$onlyPerms[ban;kick;:x: You need ban and kick permissions]`
})
```

