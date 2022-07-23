---
description: Publishing messages.
---

# $messagePublish

This function will publish the message on the servers followed your *announcement* type channel.[^1]

  [^1]: Only works in announcement channels!

### Usage

```php
$messagePublish[messageID?;channelID?]
```

### Properties

| FIELD | TYPE | DESCRIPTION |
| ----- | ----- | ----- | 
| messageID? | integer | The ID of the message we will publish  | 
| channelID? | integer | The ID of the channel |

## Example

```javascript
bot.command({
  name: "message-publish",
  code: `
  $messagePublish
  
  Hello world!
  `
  /*
    With this the bot will send a message saying, "Hello!". And once the message was sent, it will publish it.
  */
});
```
