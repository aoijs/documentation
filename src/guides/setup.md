### Installation

**node.js 16.6.0 or newer is required.**

```bash
npm install aoi.js
```

Once this has installed you can begin the following file `index.js` to setup aoi.js

```javascript
const aoijs = require("aoi.js")

const bot = new aoijs.AoiClient({
  token: "DISCORD BOT TOKEN",
  prefix: "DISCORD BOT PREFIX",
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

### package.json

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
      "node": "16.x"
    },
    "author": "",
    "license": "ISC",
    "dependencies": {
      "aoi.js": "^5.5.5"
    }
  }
```

`5.5.5` can be changed to any version number as you want.