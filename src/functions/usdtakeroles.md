---
description: Takes a role or roles from given user ID
---

# $takeRoles

This function takes the given role\(s\) from the given user

```text
$takeRoles[guildID;userID;roleID;roleID2;...]
```

```javascript
bot.command({
name: "take",
code: `$takeRoles[$guildID;$authorID;779354499865116673]`
})
```



