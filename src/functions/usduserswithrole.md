---
description: Returns a list of users with given role (members are given from the cache.)
---

# $usersWithRole

This function will return the users that have the specified role

```text
$usersWithRole[roleID;separator (optional)] //Default separator is ,
```

Lets fetch some users!

```javascript
bot.command({
name: "usersWithRole",
code: `
$usersWithRole[$roleID[Developer]]
`
})
 // Will return: Leref,Ruben
```

Now with a custom separator

```javascript
bot.command({
name: "usersWithRole",
code: `
$usersWithRole[$roleID[Developer];|] 
`
})
// Will return: Leref|Ruben
```

