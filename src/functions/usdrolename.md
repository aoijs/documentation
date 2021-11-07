---
description: Returns a Role name using their ID
---

# $roleName

This function returns the name of the specified role

```javascript
$roleName[role ID]
```

```javascript
bot.command({
name: "roleinfo", 
code: `
Role name: $roleName[$mentionedRoles[1]]
Role ID: $mentionedRoles[1]` 
})
```

