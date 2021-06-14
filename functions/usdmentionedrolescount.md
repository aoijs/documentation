---
description: Returns amount of mentioned roles in the command's message.
---

# $mentionedRolesCount

With this function you can check how many channel mentions in the command's message are.

Raw usage: `$mentionedRolesCount`

#### Example Command:

```text
bot.command({
name: "rolementions",
code: `
You have $mentionedRolesCount role mentions in your message.`
});
```

