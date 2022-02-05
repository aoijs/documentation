---
description: 'Check if the User, has Roles or Not.'
---

# $hasRoles

This function checks if the given user has the given roles. Returns boolean

```text
$hasRoles[guildID;userID;roleID;roleID;...]
```

```javascript
bot.command({
name: "role", 
code: `
$hasRoles[$guildID;$authorID;$roleID[Developer]]`
})
```

