---
description: >-
  An event that gets executed, if the bot leaves a server. To let the bot listen
  to the event, add one bot.onGuildLeave() callback inside your mainfile.
---

# bot.onGuildLeave

This callback will allow the bot to log a message whenever it leaves a server.

#### Usage:

```javascript
bot.botLeaveCommand({//command
channel: "channel id",//the channel where <code> will be sent to
code: `Your code`//message sent to <channel>
})
```

#### Example command:

```javascript
bot.botLeaveCommand({
channel: "772414449839636490",
code: `
I have left $serverName!
`
})
```

{% hint style="info" %}
You can use all guild based functions like [$serverName](../functions/usdservername.md) or [$guildID](../functions/usdguildid.md) in these commands but functions like [$getServerInvite](../functions/usdgetserverinvite.md) won't work here.
{% endhint %}

