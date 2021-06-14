---
description: >-
  An event that gets executed, if a user was unbanned from a server. To let the
  bot listen to the event, add one bot.onBanRemove() callback inside your
  mainfile.
---

# bot.onBanRemove

This callback allows the bot to log every time a user gets unbanned form a server.

#### Usage:

```javascript
bot.banRemoveCommand({ //command
channel: "channel id", //channel where bot logs
code: `your code` //your code
})
```

#### Example Commands:

```javascript
bot.banRemoveCommand({ 
channel: "772414449839636490",
code: `
$username was unbanned in $serverName
`
})
```

If you have server log variables, add this:

```javascript
bot.banRemoveCommand({ 
channel: "$getServerVar[variable]", //Add getServerVar to get the servers log channel (if they set it ofcourse)
code: `
$username was unbanned in $serverName
`
})
```

You can use amongst other functions these functions inside your banAddCommand to return data of the user that got banned and the server that banned the user:

* [$username](../functions/usdusername.md)
* [$authorID](../functions/usdauthorid.md)
* [$userTag](../functions/usdusertag.md)
* [$serverName](../functions/usdservername.md)
* [$guildID](../functions/usdguildid.md)

