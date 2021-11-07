---
description: Clears the given emojis from the given message
---

# $clearReactions

This function will remove the given emoji or all the emojis from the given message

#### Fields

This function has 3 fields

1. Channel ID \(Required\)
2. Message ID \(Required\)
3. Emoji/All \(Required\)

Raw Usage: `$clearReactions[channelID;messageID;emoji/all]`

#### Options

* Channel  ID - The channel the message is from
* Message ID - The message we're clearing the reactions from
* Emoji/All - The emoji\(s\) we're clearing

#### Usage

```javascript
bot.command({
  name: "clear-reaction",
  code: `The reaction has been removed.
  $clearReaction[804505335397744650;820290083395469352;all]
  `
  //Clears all the reactions for all the users
});
```





