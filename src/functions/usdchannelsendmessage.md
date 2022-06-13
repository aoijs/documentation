---
description: Sends a message to given Channel ID
---

# $channelSendMessage

This function allows you to send a message in the channel you selected previously.

### Usage 
```php
$channelSendMessage[channelID;message;returnMessageID?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channel ID | The channel where the message is to be sent | number | yes |
|message|The message that is to be sent|number|yes|
|return ID|Whether the id of the message is to be returned or not|yes/no|no|

## Examples

- Without the optional field

```javascript
bot.command({
  name: "send",
  code: `$channelSendMessage[Channel ID;$message]`
});
```

- With the optional field

```javascript
bot.command({
  name: "send",
  code: `$channelSendMessage[Channel ID;$message;yes]`
});
```

