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

## Table Of Contents

* [About](https://www.npmjs.com/package/aoi.js#about)
  * [Setup](https://www.npmjs.com/package/aoi.js#setup)
  * [Variables](https://www.npmjs.com/package/aoi.js#variables)
  * [Events / Callbacks](https://www.npmjs.com/package/aoi.js#callbacks)
* [Additional Support](https://www.npmjs.com/package/aoi.js#methods)
  * [Slash Commands](https://www.npmjs.com/package/aoi.js#slash-commands)
  * [Music](https://www.npmjs.com/package/aoi.js#music)
* [Links](https://www.npmjs.com/package/aoi.js#links)
 


## Installation

```js
npm i aoi.js
```

- **Note:**

```python
nodejs version 16.6.0 and above is required.
```

## Setting up

```js
const Aoijs = require("aoi.js")

const bot = new Aoijs.Bot({
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


## Music

With our new addition of music properties to Aoi.js, you can use music features in v5 too.
Check out the [docs](https://akaruidevelopment.github.io/music/) for more information!


## Links

Aoi.JS was made by [Aoi.JS Team](https://akarui.leref.ga)

* [Website](https://aoi.leref.ga)
* [Discord Server](https://aoi.leref.ga/invite)
* [Documentation](https://aoi.leref.ga)
* [GitHub](https://github.com/AkaruiDevelopment/aoi.js)

### Contribution

* [**Contribution GuideLines**](https://github.com/aoijs/aoi.js/blob/master/.github/CONTRIBUTING.md)
