---
description: Returns the command name
---

# $commandName

This function returns the name of the current code

#### Usage

```javascript
bot.command({
name: "myawesomecommand",
code: `The command name is $commandName`
/*
The bot would return:
"myawesomecommand"
*/
})
```

