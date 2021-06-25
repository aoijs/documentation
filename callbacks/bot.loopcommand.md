---
description: A command that gets executed in an interval as a loop.
---

# bot.loopCommand

This command loops a code to run every x **milliseconds.**

#### Properties:
`channel` - The channel ID where the code will be executed (Optional)

`every` - Every how much time the code to be executed. [MUST be in MS (milliseconds)]

`executeOnStartup` - Whether the code should start running as soon as bot gets started or not (True/False)

`code` - The code that is to be looped here

#### Usage:

```javascript
bot.loopCommand({
code: `
...
`,
channel: "channel id",
executeOnStartup: true/false,
every: ms
})
```

#### Example command:

```javascript
bot.loopCommand({
code: `
hi
`,
channel: "804505461076131840",
executeOnStartup: true,
every: 500000
})

/*
This command will send 'hi' to the given channel id every 5 minutes. 
ExecuteOnStartup means when the bot starts/comes online, the loop will start
*/
```

#### Command Handler Usage:
For people who use `bot.loadCommands()` handler.
```javascript
module.exports = ({
channel: "ID",
code: `
code here
`,
executeOnStartup: true/false,
every: (time in ms),
type: 'loopCommand'
})
```
#### Example command:

```javascript
module.exports = ({
channel: "804505461076131840",
code: `
hi
`,
executeOnStartup: true,
every: 50000,
type: 'loopCommand'
})
```
