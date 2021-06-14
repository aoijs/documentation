---
description: Kick using user ID
---

# $kick

This function kicks the specified user's ID

```javascript
$kick[userID;reason (optional)]
```

```javascript
bot.command({
name: "kick", 
code: `$kick[$mentioned[1]]`
//Kicks the mentioned user
})
```

