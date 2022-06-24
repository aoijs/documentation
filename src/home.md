---
cover: .gitbook/assets/cdd2be42-4bfb-40ea-aa19-b046eff15378.jpeg
coverY: -4.149292149292149
---

# Welcome

### aoi.js

**Welcome to the page of aoi.js Documentation**

### Introduction

![](https://aoi.js.org/assets/images/aoijs-new.png)

[![Discord Server](https://img.shields.io/discord/773352845738115102?color=5865F2\&logo=discord\&logoColor=white)](https://aoi.js.org/invite) [![NPM Version](https://img.shields.io/npm/v/aoi.js.svg?maxAge=3600)](https://www.npmjs.com/package/aoi.js) [![NPM Downloads](https://img.shields.io/npm/dt/aoi.js.svg?maxAge=3600)](https://www.npmjs.com/package/aoi.js)

#### Quick About

_**Aoi.JS is a package with simplified and ready-to-use functions for Discord Bot Developers to develop their own Discord Bots.**_

_**Aiming to be the easiest package to learn**_ _**It's swift and flexible using functions.**_

_**Open Source for the Community ❦**_

### Installation

**Node.JS 16.6.0 or newer is required.**

```sh-session
npm install aoi.js
```

### Setting up

```javascript
const aoijs = require("aoi.js")

const bot = new aoijs.Bot({
token: "DISCORD BOT TOKEN",
prefix: "DISCORD BOT PREFIX",
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

### Links

* [Website](https://aoi.js.org)
* [NPM](https://www.npmjs.com/package/aoi.js)
* [Github](https://github.com/AkaruiDevelopment/aoi.js)
* [Discord Server](https://discord.gg/HMUfMXDQsV)
* [Documentation](https://akarui.leref.ga/v/aoi.js/)
