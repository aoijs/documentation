---
description: >-
  An event that gets executed, if the bot sees a user joining a server. To let
  the bot listen to the event, add one bot.onJoined() callback inside your
  mainfile.
---

# bot.onJoined

Callback that triggers every time a user joins a server.

#### Usage:

```javascript
bot.joinCommand({ //command
channel: "channel id", //channel where it will log
code: `your code` //Message sent to <channel>
})
```

{% hint style="danger" %}
Make sure the &lt;channel&gt; is in the server. So recommended to use server variables \(if your bot isn't for 1 server\)
{% endhint %}

#### Example Command:

```javascript
bot.joinCommand({ 
channel: "782446718704812032", 
code: `
Welcome to $serverName, $username!
`
/*
Code Breakdown
$serverName - The name of the server the user joined
$username - The user who joined the server
*/
}) 
```

{% hint style="warning" %}
`GUILD_MEMBERS` intent needed! Information in the [Gateway Intents](../guide/begin/gateway-intents.md) guide.
{% endhint %}

{% hint style="info" %}
You can use all guild and member based functions like [$serverName](../functions/usdservername.md) or [$guildID](../functions/usdguildid.md) or [$username](../functions/usdusername.md) or [$authorID](../functions/usdauthorid.md) in these commands.
{% endhint %}

