---
description: Displays the server banner (If the guild has one)
---

# $serverBanner

This function displays the server's banner

```text
$serverBanner[guildID (optional);size (optional);dynamic (optional)]
```

```javascript
bot.command({
name: "serverBanner",
code: `Heres the server banner: 
$image[$serverBanner[$guildID;2048]]`
})
```

