---
description: Welcome to the Official Aoi.js Documentation Home Page.
---

## Introduction
<img src = "./.gitbook/assets/aoi.png">


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
 

## Examples

- ### Setup

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
bot.joinCommand({
        channel: "Channel ID", //Enter a Channel ID
        code: `<@$authorID> just joined, welcome!` //This can be changed
})
bot.onJoined()
```

### GitHub

* [**aoijs**](https://github.com/aoijs/aoi.js)

### Contribution

* [**Contribution GuideLines**](https://github.com/aoijs/aoi.js/blob/master/.github/CONTRIBUTING.md)

### Misc

* [**Discord Server Invite**](https://aoi.js.org/invite)
* [**Website**](https://aoi.js.org)
