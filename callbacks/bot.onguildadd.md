# bot.onGuildJoin

This callback will allow the bot to log a message whenever it joins a server.

#### Usage:

```javascript
bot.botJoinCommand({//command
channel: "channel id",//the channel where <code> will be sent to
code: `Your code`//message sent to <channel>
})
```

#### Example Command:

```javascript
bot.botJoinCommand({
channel: "772414449839636490",
code: `
Ive joined $serverName!
`
})
```

You can also have it send in the server where it joined by using [$systemChannelID](functions/usdsystemchannelid.md) or [$randomChannelID](functions/usdrandomchannelid.md).

```javascript
bot.botJoinCommand({
channel: "$systemChannelID",
code: `
Hi i am Awesome Bot and I can do many things.
`
 
})
```

> ⚠ Keep in mind: Not all servers have a system channel!

> ℹ️ You can use all guild based functions like [$serverName](functions/usdservername.md) or [$guildID](functions/usdguildid.md) or [$getServerInvite](functions/usdgetserverinvite.md) in these commands.
