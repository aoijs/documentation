---
description: A compact funcion with 17 different functionalities.
---

# $client

With this command you can get information about the bot user itself.

Raw usage: `$client[option]`

#### Usable Options:

* `name` =&gt; returns bot's username
* `id` =&gt; returns bot's user ID
* `tag` =&gt; returns bot's usertag 
* `mention` =&gt; returns bot's mention 
* `discrim` =&gt; returns bot's discriminator
* `avatar` =&gt; returns bot's profile avatar
* `presence` =&gt; return's the bot's activity status \(e.g. online\)
* `activity` =&gt; returns the bot's rich presence status
* `lastmid` =&gt; returns ID of last message sent by the bot
* `lastmcid` =&gt; returns ID of channel the bot's last message was sent
* `ispublic` =&gt; returns true/false if bot is public or not \(from the [Developer Portal](https://discord.com/developers/applications/)\)
* `mfaenabled` =&gt; return true if the bot's owner has 2FA enabled on their account
* `readyat` =&gt; returns the time the bot came online
* `readytimestamp` =&gt; returns the timestamp the bot came online
* `token` =&gt; returns the bot's token. More information: see [$clientToken](usdclienttoken.md)
* `ownerid` =&gt; returns the ID of the bot's owner or the ID of the owner of the application's team the bot belongs to
* `teamid` =&gt; returns the ID of the team the bot's application belongs to or the ownerID if bot has no team

#### Example Usage:

```text
bot.command({
name: "client",
code: `
My username is: $client[name]
`
})
```

