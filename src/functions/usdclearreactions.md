---
description: Clears the given emojis from the given message
---

# $clearReactions

This function will remove the given emoji or all the emojis from the given message

### Usage 
```php
$clearReactions[channelID;messageID;emoji/all?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channel ID | The id of the channel where the message is present | number | yes |
| message ID | The id of the message where reaction is present |number|yes|
|emoji|The emoji to be deleted|emoji/all|no|

## Example

```javascript
bot.command({
  name: "clear-reaction",
  code: `The reaction has been removed.
  $clearReaction[804505335397744650;820290083395469352;all]
  `
  //Clears all the reactions for all the users
});
```





