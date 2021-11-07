# Introduction

## Aoijs

**Welcome To The Home Page Of Aoi.js Documentation**

## Introduction

### Logo

![](https://aoi.js.org/assets/images/aoijs-new.png)

### Stats

[![Discord Server](https://img.shields.io/discord/773352845738115102?color=5865F2\&logo=discord\&logoColor=white)](https://aoi.js.org/invite) [![NPM Version](https://img.shields.io/npm/v/aoi.js.svg?maxAge=3600)](https://www.npmjs.com/package/aoi.js) [![NPM Downloads](https://img.shields.io/npm/dt/aoi.js.svg?maxAge=3600)](https://www.npmjs.com/package/aoi.js)

### Quick About

_**Aoi.JS is a package with simplified and ready-to-use functions for Discord Bot Developers to develop their own Discord Bots.**_

_**Aiming to be the easiest package to learn**_ _**It's swift and flexible using functions.**_

_**Open Source for the Community ❦**_

## Installation

```js
npm i aoi.js
```

**Note:**

```js
nodejs version 16.6.0 and above is required.
```

## Setting up

```javascript
 const aoijs = require('aoi.js');

 const bot = new aoijs.Bot({
   token: "Your Bot Token",
   prefix: "Bot Prefix",
   intents: "all"
 });

bot.onMessage() //enables bot to see messages (required for executing Commands)

bot.command({
  name: "ping", //command name
  code: `My Ping Is \`$ping ms\` ` //code to be executed when this command is called 
 });
```

## Quick Links

### Documentation

* [**Classes**](class/classSummary.md)
* [**Callbacks**](callbacks/CallbackSummary.md)
* [**Functions**](functions/FunctionSummary.md)
* [**Guides**](guide/GuideSummary.md)
* [**Options**](options/OptionsSummary.md)

### GitHub

* [**aoijs**](https://github.com/aoijs/aoi.js)
* [**Documentation**](https://github.com/aoijs/documentation)

### Contribution

* [**Contribution GuideLines**](https://github.com/aoijs/aoi.js/blob/master/.github/CONTRIBUTING.md)

### Misc

* [**Discord Server Invite**](https://aoi.js.org/invite)
* [**Website**](https://aoi.js.org)
