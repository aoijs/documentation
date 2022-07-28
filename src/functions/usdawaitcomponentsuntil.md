---
description: Making the bot reply to user's interacted message.
---

# $awaitComponentsUntil

This function will make the bot respond to user's select menu option or button interaction.

### Usage 

```php
$awaitComponentsUntil[channelID;messageID;filter;time;customIDs;commands;errorMessage?;data?]
```

## Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | ID of the message's channel | number | yes |
| messageID | ID of the message | number | yes |
| filter | Is it only for given user ID or everyone | string | yes |
| time | Until x time bot will response to message | string | yes |
| customIDs | Interaction ID for button/select menu | string | yes |
| commands | Awaited commands to be triggered | string | yes |
| errorMessage | When x time runs out, the part of bot sending message. | string | no |
| data | Await command's data | string | no |

## Example

```javascript
bot.command({
  name: "await-components-until",
  code: `
  $awaitComponentsUntil[$channelID;$get[buttonMessageID];everyone;20s;buttonCustomID;buttonCommand]
  
  $let[buttonMessageID;$sendMessage[{"content" : "Tap to button on below.", "components" : "{actionRow:{button::2:buttonCustomID:false:🙌🏻}}"};yes]]
  `
});

bot.interactionCommand({
  name: "buttonCommand",
  code: `
  $interactionReply[Hello!]
  `
});
```

