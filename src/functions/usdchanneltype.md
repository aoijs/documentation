---
description: Returns channel type
---

# $channelType

This function will show you the type of the specified channel.

#### Raw Usage: 
```php
$channelType[channelID (optional)]
```

## Types:

* `text` =&gt; normal text channel
* `voice` =&gt; voice channel
* `category` =&gt; category
* `news` =&gt; announcement channel

## Usage:

- Get the channel type of the current channel:

```javascript
bot.command({
  name: "type",
  code: `The type of $channelName is $channelType`
});
```

- Get the channel type of the mentioned channel:

```javascript
bot.command({
  name: "type",
  code: `The type of $channelName[$mentionedChannels[1]] is $channelType[$mentionedChannels[1]]`
});
```

