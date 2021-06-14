---
description: Sends a message to given Channel ID
---

# $channelSendMessage

This function allows you to send a message in the channel you selected previously.

#### Fields

This function has 2 required fields

1. Channel ID \(Required\)
2. Message \(Required\)
3. Return messageID  \(Optional\)

Raw Usage: `$channelSendMessage[channelID;message;returnMessageID (yes/no) (optional)]`

#### Options

* Channel ID - The channel the message is being sent
* Message - The message that's being sent
* Message ID - The ID of the message thats being sent

#### Usage

Without the optional field

```javascript
bot.command({
  name: "send",
  code: `$channelSendMessage[Channel ID;$message]`
});
```

With the optional field

```javascript
bot.command({
  name: "send",
  code: `$channelSendMessage[Channel ID;$message;yes]`
});
```

