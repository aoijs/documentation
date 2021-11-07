---
description: Function that is used in bot.onFunctionError callback.
---

### Usage:
```javascript
$handleError[option]
```

### Example:
```javascript
bot.functionErrorCommand({
channel: "832704676096245800",
code: `Error: $handleError[error]`
})
bot.onFunctionError()
```

Properties that can be used with $handleError are 
- `function` - Function Name
- `command` - Command  Name
- `error` - Returns Error

For more usage example check [bot.functionErrorCommand](../callbacks/bot.functionErrorCommand.md)

Callback for this command: [bot.onFunctionError](../callbacks/bot.onFunctionError.md)