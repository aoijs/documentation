---
description: Check if the user is a bot or not using ID
---

# $isBot

This function checks if the given user ID is a bot. Returns boolean

```text
$isBot[User ID]
```

```javascript
bot.command({
name: "isbot", 
code: `$isBot[$authorID]`
})
```

