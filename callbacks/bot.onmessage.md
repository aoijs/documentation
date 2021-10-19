# bot.onMessage

This callback is the base to running commands. It will track every message sent. You can NOT use it as an xp system. Instead, use [$alwaysExecute](functions/usdalwaysexecute.md).

```javascript
const Aoi = require("aoi.js") //allows the use of Aoi.js

const bot = new Aoi.Bot({ //makes your new bot client
token: "token", 
prefix: "prefix"
})

bot.onMessage() //allows commands to be made
```

This will allow all the commands and callbacks \(bot.command, bot.updateCommand, etc\) to run

Hey, did you know you could allow commands to work in dms? Just do this

```javascript
const Aoijs = require("aoi.js") //allows the use of Aoi.js

const bot = new Aoijs.Bot({ //makes your new bot client
token: "token", 
prefix: "prefix"
})

bot.onMessage({
  guildOnly: false //Allows commands to be ran in DMs
})
```

> ❗ bot.onMessage\(\) is necessary to make your bot work.
