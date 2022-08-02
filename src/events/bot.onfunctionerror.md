---
description: It makes the Client send the error to a specific channel.
---

# bot.onFunctionError

Property that can be used:

* `channel`

Function that can be used [$handleError](../../events/..functions/usdhandleerror.md)

Callback to use is `bot.onFunctionError()`

### Usage:

```javascript
bot.functionErrorCommand({
channel: "channel id",
code: `your code`
})

bot.onFunctionError()
```

### Example Command:

Non-Command Handler:

```javascript
bot.functionErrorCommand({
channel: "832704676096245800",
code: `$title[Error Occurred in $serverName]
$description[Function: $handleError[function]
Command: $handleError[command]
Error: $handleError[error]]
$color[RED]`
})

bot.onFunctionError()
```

Command Handler:

```javascript
//In your commands folder
module.exports = ({
type: "functionErrorCommand",
channel: "832704676096245800",
code: `$title[Error In $serverName]
$description[Function: $handleError[function]
Command: $handleError[command]
Error: $handleError[error]]
$color[RED]`
})

//In your index.js file
bot.onFunctionError()
```

You can also use

* `$channelUsed`
* `$guildID`
* `$authorID`
