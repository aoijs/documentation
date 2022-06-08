---
description: Making the bot reply to user's reacted emoji.
---

# $awaitMessageReactions

This function will make the bot reply when a user reacts with the given emoji to the command.

### Usage

```php
$awaitMessageReactions[channelID;messageID;filter;time;reactions;commands;errorMessage?;data?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | ID of the message's channel | number | yes |
| messageID | ID of the message | number | yes |
| filter | Is it only for given user ID or everyone | string | yes |
| time | Until x time bot will reply to message | string | yes |
| reactions | The reactions for respond | string | yes |
| commands | Awaited commands to be triggered | string | yes |
| errorMessage | When x time runs out, the part of bot sending message. | string | no |
| data | Await command's data | string | no |

## Example

```javascript
bot.command({
  name: "await-message-reactions",
  code: `
  $awaitMessageReactions[$channelID;$messageID;$authorID;10s;🙌🏻;raiseHands]
  `
});

bot.awaitedCommand({
  name: "raiseHands",
  code: `
  Hello!
  `
});
```

