---
description: 'Returns, True or False, if the assigned Author ID, has it.'
---

# $hasPerms

This function checks if the given user has the given permission. Returns boolean

```javascript
bot.command({
name: "check", 
code: `
$hasPerms[$guildID;$authorID;admin]`
/*
This will check if the author in a particular guild has the permission 'Administrator'
*/
})
```

