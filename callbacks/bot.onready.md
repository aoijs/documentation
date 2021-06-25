---
description: >-
  A command that gets executed by the bot, if the bot is back online (after bot
  was restarted) and connected to Discord again.
---

# bot.readyCommand

This command will have the bot send a given message to the given channel when it turns online.

#### Usage:

```javascript
bot.readyCommand({ //command
    channel: "channel ID", //The channel where the bot will log
    code: `your code` //Message sent to <channel>
})
```

#### Example command:

```javascript
bot.readyCommand({
    channel: "772414449839636490",
    code: `I'm online and ready!`
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
type: 'readyCommand'
})
```
#### Example command:

```javascript
module.exports = ({
channel: "854291989704343572",
code: `
$log[Ready on client $userTag[$clientID]]
`,
type: 'readyCommand'
})
```
