---
description: 'Check if the User, has the Roles or Not.'
---

# $hasRole

This function checks if the given user has the given role. Returns boolean

```javascript
$hasRole[userID;roleID;guildID (optional)]
```

```javascript
bot.command({
name: "role", 
code: `
$hasRole[$authorID;$roleID[Muwi]]`
})
```



