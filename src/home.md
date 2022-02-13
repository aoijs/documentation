---
coverY: 0
---

# 👋 Introduction

## Aoi.js

**Welcome To The Home Page Of aoi.js Documentation!**

## About
<img src = "./assets/aoi.png">


Aoi.js is a package with customization and ready-to-use functions to make Discord Bots with ease.

* Interaction Commands Support
* Optimized and customizable
* 500+ functions available

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

### GitHub

* [**aoijs**](https://github.com/aoijs/aoi.js)

### Contribution

* [**Contribution GuideLines**](https://github.com/aoijs/aoi.js/blob/master/.github/CONTRIBUTING.md)

### Misc

* [**Discord Server Invite**](https://aoi.js.org/invite)
* [**Website**](https://aoi.js.org)
