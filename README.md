---
description: Welcome to the Aoi.JS Documentation Page - Functions / Callbacks
---

# Introduction

![](https://aoi.js.org/assets/images/aoijs-new.png)

## Aoi.JS

[![Discord Server](https://img.shields.io/discord/773352845738115102?color=5865F2&logo=discord&logoColor=white)](https://aoi.js.org/invite) [![NPM Version](https://img.shields.io/npm/v/aoi.js.svg?maxAge=3600)](https://www.npmjs.com/package/aoi.js) [![NPM Downloads](https://img.shields.io/npm/dt/aoi.js.svg?maxAge=3600)](https://www.npmjs.com/package/aoi.js)

### About

Aoi.JS is a package with simplified and ready-to-use functions for Discord Bot Developers to develop their own Discord Bots.

- We are aiming to be the easiest package to learn.
- It's powerful with easy-to-use functions.

- Open source to the community. 

### Installation

**Node.JS 12.0.0 or newer is required.**

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
    channel: "",
    code: `$log[Ready on $userTag[$clientID]]` //Example Ready on Client
})
```

### Features

Aoi.JS has lots of features to fit your bot's needs.

* [Music](https://aoi.leref.ga/guide/music)
* [Slash Commands](https://aoi.leref.ga/guide/advanced-guides/slash-commands) *\(and other interactions\)*
* [Custom Events](https://aoi.leref.ga/guide/extras/custom-events)
* [Sharding](https://aoi.leref.ga/guide/extras/sharding)
* [...And More](https://aoi.leref.ga/)

### Optional packages

* [@discordjs/opus](https://www.npmjs.com/package/@discordjs/opus) for encoding, primarily used for Music \(`npm install @discordjs/opus`\)
* [ffmpeg-static](https://github.com/discord/ffmpeg-static) for allowing Music Filters to run smoothly \(`npm install ffmpeg-static`\)
* [danbot-hosting](https://www.npmjs.com/package/danbot-hosting) for posting stats to their API \(`npm install danbot-hosting`\)

### Links

* [Website](https://aoi.js.org)
* [Github](https://github.com/aoijs/aoi.js)
* [Discord Server](https://aoi.js.org/invite)
* [Documentation](https://aoi.leref.ga)

### Contributing

If you could like to contribute, please read [Contributing](https://github.com/aoijs/aoi.js/blob/master/.github/CONTRIBUTING.md).
