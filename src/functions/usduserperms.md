---
description: Returns all permissions the user has
---

# $userPerms

This function returns the permissions this user has

```text
$userPerms[user ID (optional);separator (optional)]
```

```javascript
bot.command({
name: "userPerms",
code: `Your Permissions: $userPerms`
//returns 'managemessages,managechannels'
})
```



