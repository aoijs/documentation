---
description: >-
  An event that gets executed, if a user was banned on a server. To let the bot
  listen to the event, add one bot.onBanAdd() callback inside your mainfile.
---

# bot.onBanAdd

This callback allows the bot to log every time someone gets banned from a server.

#### Usage:

```javascript
bot.banAddCommand({ //command
channel: "channel id", //channel where it'll be logged
code: `your code` // your code
})
```

#### Example Commands:

```javascript
bot.banAddCommand({ 
channel: "772414449839636490",
code: `$username was banned in $serverName`
})
```

If you have a server variable for logs, you can add this:

```javascript
bot.banAddCommand({ 
channel: "$getServerVar[variable]", //Add getServerVar to get the servers log channel (if they set it ofcourse)
code: `
$username was banned in $serverName
`
})
```

You can use amongst other functions these functions inside your banAddCommand to return data of the user that got banned and the server that banned the user:

* [$username](../functions/usdusername.md)
* [$authorID](../functions/usdauthorid.md)
* [$userTag](../functions/usdusertag.md)
* [$serverName](../functions/usdservername.md)
* [$guildID](../functions/usdguildid.md)

