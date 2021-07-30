---
description: It makes the bot send the error to a specific channel or if u used $log then log in the console. But it doesn't suppresses the error.
---

# bot.functionErrorCommand

Property that can be used is `channel`.

Function that can be used with it is `$handleError`.

Callback to use is `bot.onFunctionError()`.

### Usage:

```javascript
bot.functionErrorCommand({
channel: "channel id",
code: `.....`
})

bot.onFunctionError()
```

### Example:

Non-Command Handler:

```javascript
bot.functionErrorCommand({
channel: "773357157394939924",
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
module.exports =({
type: "functionErrorCommand",
channel: "773357157394939924",
code: `$title[Error In $serverName]
$description[Function: $handleError[function]
Command: $handleError[command]
Error: $handleError[error]]
$color[RED]`
})

//In your index.js file
bot.onFunctionError()
```
