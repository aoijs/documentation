---
description: Returns true/false if @everyone was mentioned in the command.
---

# $isEveryoneMentioned

With this function you can check if `@everyone` was mentioned in the command's message.

Raw usage: `$isEveryoneMentioned`

#### Example Command:

```text
bot.command({
name: "everyonementioned",
code: `
Everyone mentioned? $isEveryoneMentioned
? 
})
```

