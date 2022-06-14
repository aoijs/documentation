---
description: Clears the given emoji of the given message
---

# $clearReaction

This function will remove the given emoji for the given message ID of the given user in the given channel.

### Usage 
```php
$clearReaction[channelID;messageID;userID;emoji]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channel ID | The channel ID where the message is present | number | yes |
| message ID | The message ID where the reaction is present |number|yes|
|user ID|The id of the user whose reaction is to be deleted|number|yes|
|emoji|The emoji which is to be deleted|emoji|yes|

## Example

```javascript
bot.command({
  name: "clear-reaction",
  code: `The reaction has been removed.
  $clearReaction[804505335397744650;820290083395469352;535566311942651924;👍]
  `
});

```

