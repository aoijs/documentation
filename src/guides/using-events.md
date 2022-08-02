---
description: Here you can learn the usage of events.
---

### Using Events

### What are events?

Aoi.JS has several event listeners, called "events" to cover most events of the Discord API.

Each of them has it's own usage and own command type to run their own tasks (e.g for logging).

The events are optional except the [bot.onMessage()](../events/bot.onmessage.md) one but if you want to use them, they need to be in you main file to let the bot listen to their events and these are needed to use their different command types.

### Types of events:

#### Server based events:

* [bot.onLeave() ](../events/bot.onleave.md)=> for logging members they leave servers
* [bot.onJoin() ](../events/bot.onjoin.md)=> for logging members they join servers
* [bot.onBanAdd() ](../events/bot.onbanadd.md)=> for logging members they get banned in servers
* [bot.onBanRemove()](../events/bot.onbanremove.md) => for logging members they get unbanned inservers
* [bot.onChannelCreate() ](../events/bot.onchannelcreate.md)=> for logging channels they get created
* [bot.onChannelDelete()](../events/bot.onchanneldelete.md) => for logging channels they get deleted
* [bot.onChannelUpdate() ](../events/bot.onchannelupdate.md)=> for logging channels they get updated
* [bot.onRoleCreate() ](../events/bot.onrolecreate.md)=> for logging roles they get created
* [bot.onRoleDelete() ](../events/bot.onroledelete.md)=> for logging roles they get deleted
* [bot.onRoleUpdate() ](../events/bot.onroleupdate.md)=> for logging roles they get updated

#### Bot based events:

* [bot.onRateLimit()](../events/bot.onratelimit.md) => for logging rate limits of the bot
* [bot.onGuildJoin() ](../events/bot.onguildadd.md)=> for logging what servers the bot joins
* [bot.onGuildLeave()](../events/bot.onguildleave.md) => for logging what servers the bot leaves

#### Command & message based events:

* [bot.onMessage()](../events/bot.onmessage.md) => for logging & responding to messages
* [bot.onMessageDelete()](../events/bot.onmessagedelete.md) => for logging messages they get deleted
* [bot.onMessageUpdate()](../events/bot.onmessageupdate.md) => for logging messages they get updated
* [bot.onInteractionCreate()](variables/advanced-guides/slash-commands.md) => for using slash commands
* [bot.onReactionAdd()](../events/bot.onreactionadd.md) => for logging reactions on messages
* [bot.onReactionRemove()](../events/bot.onreactionremove.md) => for logging removed reactions on messages

#### User based events:

* [bot.onUserUpdate() ](../events/bot.onuserupdate.md)=> for logging users updating their profile
* [bot.onMemberUpdate()](../events/bot.onmemberupdate.md) => for logging members updates in a server
* [bot.onPresenceUpdate() ](../events/bot.onpresenceupdate.md)=> for logging presence updates of users
* [bot.onVoiceStateUpdate() ](../events/bot.onvoicestateupdate.md)=> for logging voice state updates of members in a server

### How to use events?

Easy! Just paste the callback you want to use in your main file below the bot creation like this:

```javascript
const aoijs = require("aoi.js")

const bot = new aoijs.Bot({
token: "DISCRD BOT TOKEN",
prefix: "DISCRD BOT PREFIX",
intents: ["GUILDS", "GUILD_MESSAGES"]
})
 
bot.onMessage() // Allows Commands to Executed
bot.onJoin() // Allows to log users joining servers
bot.onLeave() // Allows to log users leaving servers
bot.onBanAdd() // Allows to log user bans from servers
bot.onBanRemove() // Allows to log users being unbanned from servers
```

> You can add all the events you want to use for your bot.

> Each callback is only needed once. If you have events multiple times all their commands will be executed multiple times.
