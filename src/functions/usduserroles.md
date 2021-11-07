---
description: Returns all of the user's roles
---

# $userRoles

This function returns the roles that the user has

```text
$userRoles[user id;id/names/mentions (optional);separator (optional)]
```

```javascript
bot.command({
name: "userRoles",
code: `Your Roles: $userRoles[$authorID;names]`
//Will return, 'role1,role2'
})
```



