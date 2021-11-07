---
description: Returns the amount of arguments in the message of the user.
---

# $argsCount

This function will show the number of arguments in the message of the user who activated the command.

#### Usage

```javascript
bot.command({
    name: "args",
    code: `Your message has $argsCount arguments!`
});
```

