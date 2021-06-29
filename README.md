---
description: Welcome to Aoi.JS Documentarian Page - Functions / Callbacks
---

# Introduction

![aoi.js](https://camo.githubusercontent.com/5e192feb60e6fce267c34d9dd73f3f5064d6bbb391a34801ca8b42c927c0b20f/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f3830343530353436313037363133313834302f3833373139343633323134383238373530392f416f692e6a735f365f7665722e5f322e706e67)

## Aoi.JS

[![NPM Downloads](https://camo.githubusercontent.com/98d380cefe1eacf67bee86b5be3e2764650374507bc463039d3db52a4b4e6601/68747470733a2f2f696d672e736869656c64732e696f2f6e706d2f64742f616f692e6a732e7376673f6d61784167653d33363030)](https://www.npmjs.com/package/aoi.js) [![Discord Server](https://camo.githubusercontent.com/91ad6df97cc96e4b3a4afd727bf0891c89c791c2134f52e1841bce3038930707/68747470733a2f2f696d672e736869656c64732e696f2f646973636f72642f3737333335323834353733383131353130323f636f6c6f723d373238396461266c6f676f3d646973636f7264266c6f676f436f6c6f723d7768697465)](https://aoi.js.org/invite)

### Table Of Contents

* [About](https://www.npmjs.com/package/aoi.js#about)
  * [Setup](https://www.npmjs.com/package/aoi.js#setup)
  * [Variables](https://www.npmjs.com/package/aoi.js#variables)
  * [Events / Callbacks](https://www.npmjs.com/package/aoi.js#callbacks)
* [Additional Support](https://www.npmjs.com/package/aoi.js#methods)
  * [Slash Commands](https://www.npmjs.com/package/aoi.js#slash-commands)
  * [Music](https://www.npmjs.com/package/aoi.js#music)
* [Links](https://www.npmjs.com/package/aoi.js#links)

### About

Aoi.JS is a package with simplified and ready-to-use functions for Discord Bot Developers to develop their own Discord Bots.

Aiming to be the easiest package to learn   
It's swift and flexible using functions. 

Open Source for the Community ❤️ 

### Examples

#### Setup

```js
const Aoijs = require("aoi.js")

const bot = new Aoijs.Bot({
intents:["GUILDS","GUILD_MESSAGES"],
token: "TOKEN", //Discord Bot Token
prefix: "!" //Customizable
})
bot.onMessage() //Allows to run Commands

bot.command({
name: "ping", //Trigger name (command name)
code: `$ping Pong!` //Code
})

bot.readyCommand({
    channel: "", //You can use this or not.
    code: `$log[Ready on $userTag[$clientID]]` //Enter the code / message.
})
```

#### Variables

What are variables?

Variables are Key-Value based data which is stored in the database, useful for Economy and Leveling system as it is allows you to save data.

```js
bot.variables({
  VariableName1: "Value", //Returns "Value"
  VariableName2: "Value2" //Returns "Value2"
})
```

#### Callbacks

What are callbacks?

It's simple and easy process, it essentially allows you to trigger events, such as user joining a Guild. This will trigger an event, causing commands with supported type for each callbacks to be executed such as.

```js
bot.joinCommand({
        channel: "Channel ID", //Enter a Channel ID
        code: `<@$authorID> just joined, welcome!` //This can be changed
})
bot.onJoined()
```

### Additional Support

#### Slash Commands

With easy and simple functions, you can make Slash Commands with your Bots quick!

```js
bot.command({
    name: "slash",
    code: `$createSlashCommand[$guildID;version;Returns Aoi.js Version]`
})
bot.interactionCommand({
    name: "version", 
    code: `$interactionReply[$packageVersion]`
})
bot.onInteractionCreate()
```

More Information in our [Documentation](https://aoi.leref.ga/guide/slash-commands)

**Music**

With our powerful Package, we incorporated Music with several functions. We allowed customization and control over what you want.

**Music Setup Example**

```js
bot.command({
name: "play", //Trigger name (command name)
code: `$playSong[song;leave vc time;defean (yes or no);leave when vc empty (yes/no);error]`
//Code
})
```

More Information in our [Documentation](https://aoi.leref.ga/guide/music)

### Links

Aoi.JS was made by [Aoi.JS Team](https://aoi.js.org)

* [Website](https://aoi.js.org)
* [Discord Server](https://aoi.js.org/invite)
* [Documentation](https://aoi.leref.ga)

## 



