---
description: 'A command that gets executed, whenever the music queue ended.'
---

# bot.musicEndCommand

#### Usage:

```javascript
bot.musicEndCommand({ //Command
channel: "channel", //Channel where the logs are going
code: `your code` //Code
})
```

#### Example Command:

This command triggers everytime the music playback ends in a server. $channelID is where the play song command was executed.

```javascript
bot.musicEndCommand({ 
channel: "$channelID", 
code: `The music queue ended!` 
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
type: 'musicEndCommand'
})
```
#### Example command:

```javascript
module.exports = ({
channel: "705681477169315863",
code: `
The music queue ended!
`,
type: 'musicEndCommand'
})
```
