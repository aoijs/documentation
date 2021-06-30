---
description: Command Handlers can be used for organizing your commands
---

# Command Handler

## **Your main file**

Main file will allow the bot to be ran, and commands to be kept This can be named server.js, index.js whatever you want

```javascript
const Aoijs = require("aoi.js")

const bot = new Aoijs.Bot({
  sharding: false, //true or false 
  shardAmount: 2, //Shard amount 
  mobile: false, //true or false - Discord Mobile Status
  //dbhToken: "API KEY", Remove // if using, get an API Key from their Server
  token: "TOKEN", //Discord Bot Token
  prefix: ["PREFIX"], //Change PREFIX to your Prefix
  autoUpdate: false // set to true if version should be updated automatically after a package update
})

bot.onMessage() // Allows Commands to Executed
bot.loadCommands(`./commands/`) //Allows Commands executed by `commands` folder
bot.command({
name: "ping", 
code: `Pong! \`$ping\`` 
})
```

## Command Handler File Setups

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

### Now to insert your normal code:

```javascript
module.exports = {
      name: "name",
      code: `your code/message`
}
```

## Using different command types \(e.g. commands from callback events\) in the command handler:

For other commands, like the bot.joinCommand, you just have to find the part behind `bot.`- take it and insert this part at the type option as in the example below. `bot.joinCommand` becomes `type: 'joinCommand',` and  
`bot.userUpdateCommand` becomes `type: 'userUpdateCommand'` etc. like in the code below.  
The type line isn't needed for normal `bot.command` commands. Just write your code like in the code block above.

```javascript
module.exports = {
      type: 'joinCommand',
      channel: "$systemChannelID",
      code: `your code/message`
}
```

## Multiple commands in one file:

If you want to use multiple commands inside one command handler file, do it like this:

```javascript
module.exports = [{
  type: 'joinCommand'
  channel: '773364744240496640',
  code: `Welcome $userTag !!`,
}, {
  name: 'ping',
  code: `Pong! $pingms`
}]
```

### YouTube Tutorial: How to use different command types in command handler \|\| Aoi.JS

{% hint style="info" %}
Check out the YouTube tutorial [How to use Callbacks in Handler](https://www.youtube.com/watch?v=_g2M8UdsctA) on Aoi.JS
{% endhint %}

