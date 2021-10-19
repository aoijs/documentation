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

