---
description: A command that gets executed everytime the bot starts playing a new song.
---

# bot.musicStartCommand

#### Usage:

```javascript
bot.musicStartCommand({ 
channel: "channel", //Channel where the logs are going
code: `your code` //Code
})
```

#### Example Command:

This command triggers whenever a new song starts to play. You can use[ $songInfo](../functions/usdsonginfo.md) in the code to show information about the new song. $channelID is where the play command was executed.

```javascript
bot.musicStartCommand({ 
channel: "$channelID", 
code: `Now Playing: $songInfo[title] of $songInfo[publisher]` 
})

```

#### Command Handler Usage:
For people who use `bot.loadCommands()` handler.
```javascript
module.exports = ({
channel: "ID",
code: `
code here
`,
type: 'musicStartCommand'
})
```
#### Example command:

```javascript
module.exports = ({
channel: "705681477169315863",
code: `
Now Playing: $songInfo[title] of $songInfo[publisher]
`,
type: 'musicStartCommand'
})
```

