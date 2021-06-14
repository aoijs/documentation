---
description: Allows the command to be only executable in the given channel
---

# $onlyForChannels

This function only allows the command to be ran in the specified channels

```text
$onlyForChannels[channelID;channelID;...;error when not in given channels]
```

```javascript
bot.command({
name: "special",
code: `Special Command
$onlyForChannels[773353953269252127;:x: Command not executable here]`
})
```

