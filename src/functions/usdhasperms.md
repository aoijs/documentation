---
description: 'Returns, True or False, if the assigned Author ID, has it.'
---

# $hasPerms

This function checks if the given user has the given permission. Returns boolean

```javascript
bot.command({
name: "check", 
code: `
$hasPerms[$authorID;admin]`
/*
This will check if the author has the permission 'Administrator'
*/
})
```

