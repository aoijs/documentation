---
description: Allows command to be ran in only NSFW marked channel
---

# $onlyNSFW

This function only allows the command to be ran in NSFW marked channels

```
$onlyNSFW[error when ran in non-nsfw channel]
```

```javascript
bot.command({
name: "special",
code: `Special Command
$onlyNSFW[Command only executable in NSFW channels!]`
})
```

![](<../../.gitbook/assets/image (38) (1).png>)
