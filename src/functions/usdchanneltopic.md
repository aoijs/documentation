---
description: Returns the channel's topic
---

# $channelTopic

With this function you will be able to collect channel data, specifically the topic of the channel.

### Usage 
```php
$channelTopic[channelID?]
```
### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channel ID | The id of the channel whose topic is to be returned | number | no |


## Example

- Get the topic of the current channel

```javascript
bot.command({
  name: "topic",
  code: `The topic of <#$channelID> is: $channelTopic`
});
```

- Get the topic of the mentioned channel

```javascript
bot.command({
  name: "topic",
  code: `The topic of <#$mentionedChannels[1]> is: $channelTopic[$mentionedChannels[1]]`
});
```

