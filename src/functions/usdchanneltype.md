---
description: Returns channel type
---

# $channelType

This function will show you the type of the specified channel.

### Usage 
```php
$channelType[channelID?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channel ID | The id of the channel | number | no |


#### Types:

* `text` =&gt; normal text channel
* `voice` =&gt; voice channel
* `category` =&gt; category
* `news` =&gt; announcement channel
* `stage` =&gt; stage channel
* `dm` =&gt; dm channel
* `groupdm` =&gt; group dm channel
* `store` =&gt; store channel
* `newsthread` =&gt; thread in announcement channel
* `publicthread` =&gt; public thread channel
* `privatethread` =&gt; private thread channel

## Examples

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

