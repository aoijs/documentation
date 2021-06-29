---
description: Command Handlers can be used for organizing your commands
---

# Command Handler

### **Your main file** 

Main file will allow the bot to be ran, and commands to be kept This can be named server.js, index.js whatever you want

```javascript
const Aoijs = require("aoi.js")
 
const bot = new Aoijs.Bot({
  intents:["GUILD","GUILD_MESSAGES"],
  token: "TOKEN", //Discord Bot Token
  prefix: ["PREFIX"], //Change PREFIX to your Prefix
  autoUpdate: false, // set to true if version should be updated automatically after a package update
})
const loader = new Aoijs.LoadCommands(bot,true)
loader.load(bot.cmd,"./commands/",true)
bot.onMessage() // Allows Commands to Executed

bot.command({
name: "ping", 
code: `Pong! \`$ping\`` 
})
```

### Command Handler File Setups

{% hint style="warning" %}
Create a folder named "commands"
{% endhint %}

![](../../.gitbook/assets/screenshot-2020-11-23-at-9.54.22-pm.png)

{% hint style="warning" %}
Make a subfolder
{% endhint %}

![Subfolder could be used as a category like a discord category](../../.gitbook/assets/screenshot-2020-11-23-at-9.57.28-pm.png)

{% hint style="warning" %}
Finally, make your file
{% endhint %}

![Name of file: commandName.js](../../.gitbook/assets/screenshot-2020-11-23-at-10.00.16-pm.png)

#### Now to insert your normal code:

```javascript
module.exports = {
      name: "name",
      code: `your code/message`
}
```

### Using different command types \(e.g. commands from callback events\) in the command handler:

For other commands, like the bot.joinCommand,`type` will be more close to the callback or part after removing `bot.` and `Command` as in the example below. `bot.joinCommand` becomes `type: 'join',` and   
`bot.userUpdateCommand` becomes `type: 'userUpdate'` etc. like in the code below.  
The type line isn't needed for normal `bot.command` but u can use "default" for them in commands. Just write your code like in the code block above.

```javascript
module.exports = {
      type: 'join',
      channel: "$systemChannelID",
      code: `your code/message`
}
```

### Multiple commands in one file:

If you want to use multiple commands inside one command handler file, do it like this:

```javascript
module.exports = [{
  type: 'join'
  channel: '773364744240496640',
  code: `Welcome $userTag !!`,
}, {
  name: 'ping',
  code: `Pong! $pingms`
}]
```

#### Types
**ALL AVAILABLE TYPES ARE:**
```js
//GUILD_MESSAGES INTENTS 
"default" 
"awaited"
"messageDelete" 
"messageUpdate" 
"messageDeleteBulk" 
//GUILDS INTENTS
"guildJoin"
"guildUpdate"
"guildLeave"
"guildUnavailable"
"roleCreate"
"roleUpdate"
"roleDelete"
"channelCreate"
"channelUpdate"
"channelDelete"
"channelPinsUpdate"
"stageIntanceCreate"
"stageIntanceUpdate"
"stageIntanceDelete"
//GUILD_MEMBERS INTENT 
"join"
"leave"
"memberUpdate"
"memberAvailable"
"memberChunk"
//GUILD_EMOJIS INTENT 
"emojiCreate"
"emojiUpdate"
"emojiDelete"
//GUILD_BANS INTENT 
"banAdd"
"banRemove"
//GUILD_WEBHOOKS INTENT 
"webhookUpdate"
//GUILD_INVITES INTENT
"inviteCreate"
"inviteDelete"
//GUILD_VOICE_STATES INTENT
"voiceStateUpdate"
//GUILD_PRESENCES INTENT
"presenceUpdate"
//GUILD_MESSAGE_REACTIONS INTENT
"reactionAdd"
"reactionRemove"
"reactionRemoveEmoji"
"reactionRemoveAll"
//GUILD_TYPING_START INTENT 
"typingStart"
//no intent required 
"loop"
"timeout"
"pulse"
"ready"
"variableCreate"
"variableDelete"
"variableUpdate"
"functionError"
"interaction"
"applicationCmdCreate"
"applicationCmdUpdate"
"applicationCmdDelete"
"userUpdate"
"rateLimit"
"musicStart"
"musicEnd"  
```

