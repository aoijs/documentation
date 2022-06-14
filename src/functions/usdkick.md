---
description: Kick using user ID
---

# $kick

This function kicks the specified user's ID

```javascript
$kick[guildID;userID;reason (optional)]
```

```javascript
bot.command({
name: "kick", 
code: `$kick[$guildID;$mentioned[1]]`
//Kicks the mentioned user
})
```

