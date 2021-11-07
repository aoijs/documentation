---
description: This page will help begin your New Bot!
---

## Installation

{% hint style="warning" %}
**node.js 16.6.0 or newer is required.**
{% endhint %}

{% tabs %}
{% tab title="Terminal" %}
```bash
npm install aoi.js
```
{% endtab %}
{% endtabs %}

Once this has installed you can begin the following file `index.js` to setup aoi.js

{% tabs %}
{% tab title="index.js" %}
```javascript
const aoijs = require("aoi.js")

const bot = new aoijs.Bot({
token: "TOKEN", //Discord Bot Token
prefix: "PREFIX", //Discord Bot Prefix
intents: "all" //Discord Intents
})

//Events
bot.onMessage()

//Command Example
bot.command({
name: "ping",
code: `Pong! \`$ping\`ms`
})

//Ready Event
bot.readyCommand({
    channel: "",
    code: `$log[Ready on $userTag[$clientID]]`
})
```
{% endtab %}
{% endtabs %}

## package.json

The file where your project can "get" aoi.js

```javascript
{
    "name": "-asdf",
    "version": "1.0.0",
    "description": "",
    "main": "index.js",
    "scripts": {
      "start": "node index.js"
    },
    "engines": {
      "node": "16.6"
    },
    "author": "",
    "license": "ISC",
    "dependencies": {
      "aoi.js": "^5.0.0"
    }
  }
```

{% hint style="info" %}
`5.0.0` can be changed to any version number as you want.
{% endhint %}