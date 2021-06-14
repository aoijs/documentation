---
description: Sends message to specified channel
---

# $useChannel

This function sends a message to the given channel

```javascript
$useChannel[channel ID]
```

```javascript
bot.command({
name: "useChannel",
code: `Hi!
$useChannel[773363417338609674]` //Sends 'Hi!' in the given channel
})
```

