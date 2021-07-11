---
description: Here you can learn the usage of callbacks.
---

# Using Callbacks

### What Are Callbacks?

Aoi.JS has several event listeners, called "callbacks" to cover most events of the Discord API.

Each of them have their own usage and command type, to run their own tasks \(e.g logging\).

All callbacks are optional except the [bot.onMessage\(\)](../../callbacks/bot.onmessage.md) one. If you want to use certain callbacks, they need to be in your main file to let the bot listen to their events and use their different command types.

### Types of Callbacks
* [bot.onBanAdd\(\) ](../../callbacks/bot.onbanadd.md)
* [bot.onBanRemove\(\)](../../callbacks/bot.onbanremove.md)
* [bot.onChannelCreate\(\) ](../../callbacks/bot.onchannelcreate.md)
* [bot.onChannelDelete\(\)](../../callbacks/bot.onchanneldelete.md)
* [bot.onChannelUpdate\(\) ](../../callbacks/bot.onchannelupdate.md)
* [bot.onGuildJoin\(\) ](../../callbacks/bot.onguildadd.md)
* [bot.onGuildLeave\(\)](../../callbacks/bot.onguildleave.md)
* [bot.onInteractionCreate\(\)](../advanced-guides/slash-commands.md)
* [bot.onInviteCreate\(\) ](../../callbacks/bot.oninvitecreate.md)
* [bot.onInviteDelete\(\)](../../callbacks/bot.oninvitedelete.md)
* [bot.onJoined\(\) ](../../callbacks/bot.onjoined.md)
* [bot.onLeave\(\) ](../../callbacks/bot.onleave.md)
* [bot.onMemberUpdate\(\)](../../callbacks/bot.onmemberupdate.md)
* [bot.onMessage\(\)](../../callbacks/bot.onmessage.md)
* [bot.onMessageDelete\(\)](../../callbacks/bot.onmessagedelete.md)
* [bot.onMessageUpdate\(\)](../../callbacks/bot.onmessageupdate.md)
* [bot.onPresenceUpdate\(\) ](../../callbacks/bot.onpresenceupdate.md)
* [bot.onRateLimit\(\)](../../callbacks/bot.onratelimit.md)
* [bot.onReactionAdd\(\)](../../callbacks/bot.onreactionadd.md)
* [bot.onReactionRemove\(\)](../../callbacks/bot.onreactionremove.md)
* [bot.onRoleCreate\(\) ](../../callbacks/bot.onrolecreate.md)
* [bot.onRoleDelete\(\) ](../../callbacks/bot.onroledelete.md)
* [bot.onRoleUpdate\(\) ](../../callbacks/bot.onroleupdate.md)
* [bot.onUserUpdate\(\) ](../../callbacks/bot.onuserupdate.md)
* [bot.onVoiceStateUpdate\(\) ](../../callbacks/bot.onvoicestateupdate.md)

### Using Callback

Easy! Just paste the callback you want to use in your main file, below the bot creation. Like this:

```javascript
const Aoijs = require("aoi.js")
 
const bot = new Aoijs.Bot({
  token: "TOKEN", //Discord Bot Token
  prefix: ["PREFIX"] //Change PREFIX to your Prefix
})
 
bot.onMessage() // Allows Commands to Executed
bot.onJoined() // Allows to log users joining servers
bot.onLeave() // Allows to log users leaving servers
bot.onBanAdd() // Allows to log user bans from servers
bot.onBanRemove() // Allows to log users being unbanned from servers
```

{% hint style="success" %}
You can add all the callbacks you want to use for your bot.
{% endhint %}

{% hint style="warning" %}
Each callback is only needed once. If you have callbacks listed multiple times, all their commands will be executed multiple times.
{% endhint %}
