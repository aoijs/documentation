---
coverY: 0
---

# Introduction

## aoi.js

**Welcome To The Home Page Of aoi.js Documentation**

### About

aoi.js is a package with customization and ready-to-use functions to make Discord Bots with ease.

* Interaction Commands Support
* Optimized and customizable
* 500+ functions available

## Installation

```js
npm i aoi.js
```

**Note:**

```python
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

### GitHub

* [**aoijs**](https://github.com/aoijs/aoi.js)

### Contribution

* [**Contribution GuideLines**](https://github.com/aoijs/aoi.js/blob/master/.github/CONTRIBUTING.md)

### Misc

* [**Discord Server Invite**](https://aoi.js.org/invite)
* [**Website**](https://aoi.js.org)
