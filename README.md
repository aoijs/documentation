---
description: Welcome to the Official Aoi.js Documentation Home Page.
---

## Introduction
<img src = "./src/assets/aoi.png">


[![Discord Server](https://img.shields.io/discord/773352845738115102?color=5865F2\&logo=discord\&logoColor=white)](https://aoi.js.org/invite) [![NPM Version](https://img.shields.io/npm/v/aoi.js.svg?maxAge=3600)](https://www.npmjs.com/package/aoi.js) [![NPM Downloads](https://img.shields.io/npm/dt/aoi.js.svg?maxAge=3600)](https://www.npmjs.com/package/aoi.js)


## About

_Aoi.JS is a package with simplified and ready-to-use functions for Discord Bot Developers to develop their own Discord Bots._

_Aiming to be the easiest package to learn_   
_It's swift and flexible using functions._ 

_Open Source for the Community ❤️_



## Installation

**Node.JS 16.6.0 or newer is required.**  

```sh-session
npm install aoi.js
```

## Setting up

```js
const aoijs = require("aoi.js")

const bot = new aoijs.Bot({
token: "DISCRD BOT TOKEN",
prefix: "DISCRD BOT PREFIX",
intents: ["GUILDS", "GUILD_MESSAGES"]
})

//Events
bot.onMessage()

//Command Example (ping)
bot.command({
name: "ping",
code: `Pong! $pingms`
})

//Ready Event
bot.readyCommand({
    channel: "",
    code: `$log[Ready on $userTag[$clientID]]`
})
```
## Additional Settings

### Variables

- What are variables?

Variables are Key-Value based data which is stored in the database, useful for Economy and Leveling system as it is allows you to save data.

```js
bot.variables({
  VariableName1: "Value", //Returns "Value"
  VariableName2: "Value2" //Returns "Value2"
})
```

### Callbacks

- What are callbacks?

It's simple and easy process, it essentially allows you to trigger events, such as user joining a Guild. This will trigger an event, causing commands with supported type for each callbacks to be executed such as.

```js
bot.joinCommand({ //command
channel: "channel id", //channel where it will log
code: `your code` //Message sent to <channel>
})
bot.onJoin()
```

### Slash Commands

- With easy and simple functions, you can make Slash Commands with your Bots quick!

```js
bot.command({
name: "create",
code: `$createApplicationCommand[$guildID;aoijs;a cool slash command for aoi.js;true]`
/*
    Code Breakdown:
This will make a slashcommand named "aoijs" (meaning you'd do /aoijs),
the description will say "a cool slash command for aoijs"
*/
})

// Initializing the slash command

bot.interactionCommand({
name: "aoijs", 
prototype : 'slash',
code: `$interactionReply[AOIjs is an awesome package!]`
/*
The code will be execute once /aoijs has been ran
*/
})
bot.onInteractionCreate()

```

### Custom Functions for Intermediate Developers
- With the latest feature of aoi.js v5.0.0 and above, which enables Developers to create their own custom function built-in and easy.

```js
/*THIS IS JUST AN EXAMPLE IN YOUR MAIN FILE*/

const aoijs = require("aoi.js")

const bot = new aoijs.Bot({
token: "DISCRD BOT TOKEN",
prefix: "DISCRD BOT PREFIX",
intents: ["GUILDS", "GUILD_MESSAGES"]
})

//Events
bot.onMessage()

/*CREATING THE ACTUAL FUNCTION*/
/*EXAMPLE OF MAKING $authorOnlyButton*/

bot.functionManager.createCustomFunction({
name : '$authorOnlyButton', //FUNCTION NAME 
params : ['index','label','style','customId','disabled','emoji'],//THE TYPE OF PARAMS
type : 'aoi.js', //TYPE METHOD
code : ` 
$addButton[{index};{label};{style};{customId}_$authorId;{disabled};{emoji}]
` //THE ACTUAL CODE IT WILL BE RETURN
})

/*ONLY EXPERIENCED WITH UNDERSTANDING OF AOIJS SHOULD USE*/

/*BY USING CUSTOM FUNCTION WE ARE'T OBLIGED OF WHAT HAPPENS TO YOUR CLIENT*/

/*WITH THIS FUNCTION MANAGER IT JUST CREATED $authorOnlyButton function*/
```


## Music

With our new addition of music properties to Aoi.js, you can use music features in v5 too.
Check out the [docs](https://akaruidevelopment.github.io/music/) for more information!

## Links
- [Website](https://aoi.js.org)
- [NPM](https://www.npmjs.com/package/aoi.js)
- [Github](https://github.com/AkaruiDevelopment/aoi.js)
- [Discord Server](https://discord.gg/HMUfMXDQsV)
- [Documentation](https://akarui.leref.ga/v/aoi.js/)
