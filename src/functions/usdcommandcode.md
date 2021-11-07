---
description: Returns the current command's code
---

# $commandCode

This function returns the current commands code

#### Usage

```javascript
bot.command({
name: "expose-code",
code: `Command Code: $commandCode`
/*
Bot would return
"Command Code: $commandCode"
*/
})
```

