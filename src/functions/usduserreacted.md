---
description: Returns boolean of user reacted to message, or not.
---

# $userReacted

This function will return `true` or `false` depending if the user reacted with given emoji to given message ID.

### Usage

```php
$userReacted[channelID;messageID;userID;emoji]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The ID of the channel | number | yes |
| messageID | The ID of the message | number | yes |
| userID | The ID of the user | number | yes |
| emoji | The emoji of the message we will check | string | yes |

## Example

```javascript
bot.command({
  name: "users-reacted",
  code: `
  $userReacted[784626845059383316;808044141048627260;$authorID;<:checkmark:805116425345302528>]
  `
// This will check if the user reacted with the :checkmark: emoji to one of my tips.
});
```
