---
description: Checks if user is banned. Returns true or false
---

# $isBanned

This  function checks if the given user is banned or not. Returns boolean

```text
$isBanned[user ID;guild ID (optional)]
```

```javascript
bot.command({
name: "isBanned",
code: `Is banned: $isBanned[535566311942651924]`
})
```

