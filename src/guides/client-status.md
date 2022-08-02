---
description: How to setup a Bot Status
---

### Setting a Client Status:

You need to enter the following, in your main index.

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

If you want to change the Client Discord Status use the following:

```diff
+ status: "type"
```

```javascript
bot.status({
  text: "TEXT",
  type: "PLAYING",
  status: "idle",
  time: 12
})
```

### Different Status Types:

* `idle`
* `dnd`
* `online`
* `invisible`

### Streaming URL Method:

Streaming-Status supports `YouTube-Video-URLs` or `Twitch-Stream-URLs`.

If you want to enter an URL, Enter the following
 
```diff
+ url: "URL"
```

```javascript
bot.status({
text: "TEXT", 
type: "STREAMING", 
url: "URL"
})
```

> Make sure your `type` is `STREAMING`

### Mobile Status

```diff
+ mobilePlatform: true
```

```javascript
const aoijs = require("aoi.js")

const bot = new aoijs.AoiClient({
  token: "DISCORD BOT TOKEN",
  prefix: "DISCORD BOT PREFIX",
  intents: ["GUILDS", "GUILD_MESSAGES"]
})
mobilePlatform: true
})
```

![Example](<../discord-examples/assets/image (62).png>)