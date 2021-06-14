---
description: Clears the given emoji of the given message
---

# $clearReaction

This function will remove the given emoji for the given message ID of the given user in the given channel.

#### Fields

This function has 4 fields

1. Channel ID \(Required\)
2. Message ID \(Required\)
3. User ID \(Required\)
4. Emoji \(Required\)

Raw Usage: `$clearReaction[channelID;messageID;userID;Emoji]`

#### Options

* Channel  ID - The channel the message is from
* Message ID - The message we're clearing the reactions from
* User ID - The user's reaction we're clearing
* Emoji - The emoji we're clearing

#### Usage

```javascript
bot.command({
  name: "clear-reaction",
  code: `The reaction has been removed.
  $clearReaction[804505335397744650;820290083395469352;535566311942651924;👍]
  `
});

```

