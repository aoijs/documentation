---
description: The page to guide you with Aoi.JS.
---

# Getting Started

## Installation

{% hint style="warning" %}
**Node.JS 12.0.0 or newer is required.**
{% endhint %}

{% tabs %}
{% tab title="Terminal" %}
```bash
npm install aoi.js
```
{% endtab %}
{% endtabs %}

Once this has installed you can begin the following file `index.js` to setup Aoi.JS.

{% tabs %}
{% tab title="index.js" %}
```javascript
const aoijs = require("aoi.js")

const bot = new aoijs.Bot({
token: "TOKEN", //Discord Bot Token
prefix: "PREFIX" //Discord Bot Prefix
})
bot.onMessage() //Allows to execute Commands

bot.command({
name: "ping", //Trigger name (command name)
code: `Pong! \`$ping\`ms` //Code
})

bot.readyCommand({
    channel: "", //You can use this or not
    code: `$log[Ready on $userTag[$clientID]]` //Example Ready on Client
})
```
{% endtab %}
{% endtabs %}

> You must enter a prefix via `PREFIX`
>
> You must enter a valid Discord Bot Token via `TOKEN`

{% hint style="success" %}
Just simple as that you can begin using Aoi.JS
{% endhint %}

## package.json

{% hint style="warning" %}
In most Hosting Services you will need a `package.json` file
{% endhint %}

If you need a example, there's a quick example to use.

{% tabs %}
{% tab title="package.json" %}
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
      "node": "12.x"
    },
    "author": "",
    "license": "ISC",
    "dependencies": {
      "aoi.js": "^4.5.0"
    }
  }
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
`4.5.0` can be changed to any version number as you want.
{% endhint %}

