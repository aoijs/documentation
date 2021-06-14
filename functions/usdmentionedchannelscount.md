---
description: Returns amount of mentioned channels in the command's message.
---

# $mentionedChannelsCount

With this function you can check how many channel mentions are in the command's message.

Raw usage: `$mentionedChannelsCount`

#### Example Command:

```text
bot.command({
name: "channelmentions",
code: `
You have $mentionedChannelsCount channel mentions in your message.`
});
```

