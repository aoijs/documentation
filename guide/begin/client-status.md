---
description: How to setup a Bot Status
---

# Client Status

### Setting a Client Status:

{% hint style="danger" %}
You need to enter the following, in your main index.
{% endhint %}

### Usage:

```javascript
bot.status({
  text: "TEXT",
  type: "PLAYING",
  time: 12
})
```

### Adding multiple Client Status:

```javascript
bot.status({
  text: "TEXT1",
  type: "PLAYING",
  time: 12
})

bot.status({
  text: "TEXT2",
  type: "WATCHING",
  time: 12
})
```

### Different Types:

* PLAYING
* WATCHING
* LISTENING
* STREAMING
* COMPETING

### Client Status Method:

{% hint style="info" %}
If you want to change the bot's discord status use the following
{% endhint %}

```javascript
bot.status({
  text: "TEXT",
  type: "PLAYING",
  status: "idle",
  time: 12
})
```

### Different Status:

* idle
* dnd
* online
* invisible

### Streaming URL Method:

{% hint style="info" %}
Streaming-Status supports YouTube-Video-URL or Twitch-Channel-URLs.

If you want to enter an URL, Enter the following
{% endhint %}

```javascript
bot.status({
text: "TEXT", 
type: "STREAMING", 
url: "URL"
})
```

### Mobile Status

```javascript
const aoijs = require("aoi.js")

const bot = new aoijs.Bot({
token: "TOKEN", //Discord Bot Token
prefix: "PREFIX", //Discord Bot Prefix
mobile: true //True or false
})
```

![Example](../../.gitbook/assets/image%20%2862%29.png)