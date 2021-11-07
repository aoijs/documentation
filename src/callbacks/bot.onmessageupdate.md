---
description: >-
  An event that gets executed, if the bot sees a user editing a message. To let
  the bot listen to the event, add one bot.onMessageUpdate() callback inside
  your mainfile.
---

# bot.onMessageUpdate

This callback allows the bot to log any edited messages to the given channel

#### Usage:

```javascript
bot.updateCommand({ //the command 
        channel: "the channel id", //the chanel where the bot will log
        code: `Your wonderful code` //Your code that will appear in <channel>
})
```

#### Example command:

```javascript
bot.updateCommand({
        channel: "782446718704812032", 
        code: `Message edited from $username in <#$channelUsed>:
$message
Old message: $oldMessage`
/*
        Code Breakdown
$message - The new message
$oldMessage - The message before it was edited (This function only works in this callback)
$username - The person who edited the message
$channelUsed - Where the person edited the message
*/
})
```

