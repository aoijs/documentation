---
description: Allows command to be ran in only NSFW marked channel
---

# $onlyNSFW

This function only allows the command to be ran in NSFW marked channels 

```text
$onlyNSFW[error when ran in non-nsfw channel]
```

```javascript
bot.command({
name: "special",
code: `Special Command
$onlyNSFW[Command only executable in NSFW channels!]`
})
```

![](../.gitbook/assets/image%20%2838%29%20%281%29.png)

