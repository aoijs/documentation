---
description: Aoi.JS Official Documentation - Functions / Callbacks / Examples
---

# Introduction

![](https://aoi.js.org/assets/images/aoijs-new.png)

## Aoi.JS

[![Discord Server](https://img.shields.io/discord/773352845738115102?color=5865F2&logo=discord&logoColor=white)](https://aoi.js.org/invite) [![NPM Version](https://img.shields.io/npm/v/aoi.js.svg?maxAge=3600)](https://www.npmjs.com/package/aoi.js) [![NPM Downloads](https://img.shields.io/npm/dt/aoi.js.svg?maxAge=3600)](https://www.npmjs.com/package/aoi.js)

### About

Aoi.JS is a package with simplified and ready-to-use functions for Discord Bot Developers to develop their own Discord Bots.

Aiming to be the easiest package to learn  
It's swift and flexible using functions.

Open Source for the Community ❤️

### Installation

**Node.JS 14.0.0 or newer is required.**

```text
npm install aoi.js
```

#### Example

```javascript
const aoijs = require("aoi.js")

const bot = new aoijs.Bot({
token: "TOKEN", //Discord Bot Token
prefix: "PREFIX" //Discord Bot Prefix
})
bot.onMessage() //Allows to execute Commands

bot.command({
name: "ping", //Trigger name (command name)
code: `Pong! $pingms` //Code
})

bot.readyCommand({
    channel: "", //You can use this or not
    code: `$log[Ready on $userTag[$clientID]]` //Example Ready on Client
})
```

#### Optional packages

* [@discordjs/opus](https://www.npmjs.com/package/@discordjs/opus) for encoding, primarily used for Music \(`npm install @discordjs/opus`\)
* [ffmpeg-static](https://github.com/discord/ffmpeg-static) for allowing Music Filters to run smoothly \(`npm install ffmpeg-static`\)
* [danbot-hosting](https://www.npmjs.com/package/danbot-hosting) for posting stats to their API \(`npm install danbot-hosting`\)

**Music Integration**

With our powerful Package, we incorporated Music with several functions. We allowed customization and control over what you want.

**Music Example**

```javascript
bot.command({
name: "play",
code: `$playSong[Music Name;Something went wrong!]`
})
```

More Information in our [Documentation](https://aoi.leref.ga/guide/music)

### Links

* [Website](https://aoi.js.org)
* [Github](https://github.com/aoijs/aoi.js)
* [Discord Server](https://aoi.js.org/invite)
* [Documentation](https://aoi.leref.ga)

### Contributing

Please read [Contributing](https://github.com/aoijs/aoi.js/blob/master/.github/CONTRIBUTING.md)

