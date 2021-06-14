---
description: This page will help begin your New Bot!
---

# Begin

###  **Installing Aoi.js**

```text
npm i aoi.js
```

 ![:warning:](https://canary.discord.com/assets/289673858e06dfa2e0e3a7ee610c3a30.svg) Installing Aoi.JS can be different depending on your host. Please check \#video-tutorials for exact guides. 

### **Your main file** 

Main file will allow the bot to be ran, and commands to be kept. This can be named server.js, index.js or whatever you want.

```javascript
const Aoijs = require("aoi.js")
 
const bot = new Aoijs.Bot({
  sharding: false, //true or false 
  shardAmount: 2, //Shard amount 
  mobile: false, //true or false - Discord Mobile Status
  //dbhToken: "API KEY", Remove // if using, get an API Key from their Server
  token: "TOKEN", //Discord Bot Token
  prefix: ["PREFIX"], //Change PREFIX to your Prefix
  autoUpdate: false, // set to true if version should be updated automatically after a package update
})
 
bot.onMessage() // Allows Commands to Executed
 
bot.command({
name: "ping", 
code: `Pong! \`$ping\`` 
})
```

###  P**ackage.json** 

The file where your project can "get" aoi.js

```javascript
{
    "name": "-asdf",
    "version": "1.0.0",
    "description": "",
    "main": "server.js",
    "scripts": {
      "start": "node server.js"
    },
    "engines": {
      "node": "12.x"
    },
    "author": "",
    "license": "ISC",
    "dependencies": {
      "aoi.js": "^3.0.0"
    }
  }
```

 ![:warning:](https://canary.discord.com/assets/289673858e06dfa2e0e3a7ee610c3a30.svg) To update Aoi.JS, change the version number to latest via [\#changelog ](https://discord.gg/TbvJSCsM7X)

#### **Basic Command Format**

```javascript
bot.command({
      name: "name",
      code: `your code/message`
})
```

####  **Simple Status**

```javascript
bot.status({
      text: "aoi.js",
      type: "PLAYING",
      time: 12
})
```

 ![:warning:](https://canary.discord.com/assets/289673858e06dfa2e0e3a7ee610c3a30.svg) **If you are using glitch or repl.it. Do not use `npm i aoi.js` If you add package.json, It will install the package automatically!**

