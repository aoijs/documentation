---
description: Checks if the user has at least one of the required perms
---

# $hasAnyPerm

This functionw ill check if the user has at least one of the specified perms inside of the function.

Raw usage: `$hasAnyPerm[perm1;perm2;...]` or `$hasAnyPerm[User ID;perm1;perm2;...]`

Example:

```javascript
bot.command({
    name: "hasperms",
    code: `
$hasAnyPerm[addreactions;sendmessages;manageserver]
    `
})
```

The bot will reply with `true` if the user has at least one of the 3 perms we requested, in this case `addreactions, sendmessages` or `manageserver`.

