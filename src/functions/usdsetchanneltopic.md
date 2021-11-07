---
description: Sets a channel's topic
---

# $setChannelTopic

This function allows the bot to set a &lt;channel&gt; topic

```text
$setChannelTopic[channelID;new topic] ($setChannelTopc[channel id] will remove the topic)
```

Here's a simple usage 

```javascript
bot.command({
name: "channel-topic".
code: `$setChannelTopic[$channelID;This is general chat!]`
})
```



