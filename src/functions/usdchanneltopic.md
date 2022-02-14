---
description: Returns the channel's topic
---

# $channelTopic

With this function you will be able to collect channel data, specifically the topic of the channel.

## Fields

1. Channel ID \(Required\)

#### Raw Usage: 
```php
$channelTopic[channelID]
```

## Options

* Channel ID - The channel we're getting the topic from

## Usage

- Get the topic of the current channel

```js
bot.command({
  name: "topic",
  code: `The topic of <#$channelID> is: $channelTopic[$channelID]`
});
```

- Get the topic of the mentioned channel

```js
bot.command({
  name: "topic",
  code: `The topic of <#$mentionedChannels[1]> is: $channelTopic[$mentionedChannels[1]]`
});
```

