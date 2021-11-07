---
description: Returns Guild ID.
---

# $guildID

This function return's the current guild's id

```javascript
$guildID[server name (optional)]
```

```javascript
bot.command({
name: "server", 
code: `Server Name: $serverName[$guildID] 
Guild ID: $guildID`
})
```

