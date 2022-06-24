---
description: Here you can learn the usage of callbacks.
---

# Using Events

### What are callbacks?

Aoi.JS has several event listeners, called "callbacks" to cover most events of the Discord API.

Each of them has it's own usage and own command type to run their own tasks (e.g for logging).

The callbacks are optional except the [bot.onMessage()](../callbacks/bot.onmessage.md) one but if you want to use them, they need to be in you main file to let the bot listen to their events and these are needed to use their different command types.

### Types of callbacks:

#### Server based callbacks:

* [bot.onLeave() ](../callbacks/bot.onleave.md)=> for logging members they leave servers
* [bot.onJoined() ](../guide/begin/broken-reference/)=> for logging members they join servers
* [bot.onBanAdd() ](../callbacks/bot.onbanadd.md)=> for logging members they get banned in servers
* [bot.onBanRemove()](../callbacks/bot.onbanremove.md) => for logging members they get unbanned inservers
* [bot.onInviteCreate() ](../callbacks/bot.oninvitecreate.md)=> for logging invites they get created (e.g. for [Invite-Tracking](variables/advanced-guides/invite-system.md))
* [bot.onInviteDelete()](../callbacks/bot.oninvitedelete.md) => for logging invites they get deleted
* [bot.onChannelCreate() ](../callbacks/bot.onchannelcreate.md)=> for logging channels they get created
* [bot.onChannelDelete()](../callbacks/bot.onchanneldelete.md) => for logging channels they get deleted
* [bot.onChannelUpdate() ](../callbacks/bot.onchannelupdate.md)=> for logging channels they get updated
* [bot.onRoleCreate() ](../callbacks/bot.onrolecreate.md)=> for logging roles they get created
* [bot.onRoleDelete() ](../callbacks/bot.onroledelete.md)=> for logging roles they get deleted
* [bot.onRoleUpdate() ](../callbacks/bot.onroleupdate.md)=> for logging roles they get updated

#### Bot based callbacks:

* [bot.onRateLimit()](../callbacks/bot.onratelimit.md) => for logging rate limits of the bot
* [bot.onGuildJoin() ](../callbacks/bot.onguildadd.md)=> for logging what servers the bot joins
* [bot.onGuildLeave()](../callbacks/bot.onguildleave.md) => for logging what servers the bot leaves

#### Command & message based callbacks:

* [bot.onMessage()](../callbacks/bot.onmessage.md) => for logging & responding to messages
* [bot.onMessageDelete()](../callbacks/bot.onmessagedelete.md) => for logging messages they get deleted
* [bot.onMessageUpdate()](../callbacks/bot.onmessageupdate.md) => for logging messages they get updated
* [bot.onInteractionCreate()](variables/advanced-guides/slash-commands.md) => for using slash commands
* [bot.onReactionAdd()](../callbacks/bot.onreactionadd.md) => for logging reactions on messages
* [bot.onReactionRemove()](../callbacks/bot.onreactionremove.md) => for logging removed reactions on messages

#### User based callbacks:

* [bot.onUserUpdate() ](../callbacks/bot.onuserupdate.md)=> for logging users updating their profile
* [bot.onMemberUpdate()](../callbacks/bot.onmemberupdate.md) => for logging members updates in a server
* [bot.onPresenceUpdate() ](../callbacks/bot.onpresenceupdate.md)=> for logging presence updates of users
* [bot.onVoiceStateUpdate() ](../callbacks/bot.onvoicestateupdate.md)=> for logging voice state updates of members in a server

### How to use callbacks?

Easy! Just paste the callback you want to use in your main file below the bot creation like this:

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
Each callback is only needed once. If you have callbacks multiple times all their commands will be executed multiple times.
{% endhint %}
