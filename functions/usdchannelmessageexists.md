---
description: Checks if given message exists in the given channel. Returns true/false
---

# $messageExists

This function will check if the indicated message exists on the indicated channel, as result will return true/false depending if it exists or not.

#### Fields

 This function has 2 fields

1. Channel ID 
2. Message ID

Raw Usage: `$messageExists[channelID;messageID]`

#### Options

* Channel ID - The channel of which the &lt;messageID&gt; is located in
* Message ID - The message ID that we're looking to see if it exists in &lt;channel ID&gt;

#### Usage

```javascript
bot.command({
    name: "exists",
    code: `
    The message the ID "$message[1]" in the channel <#$mentionedChannels[1;yes]> exists?
    $mssageExists[$mentionedChannels[1;yes];$message[1]]
    `
});

/* 
    The use of this command would be
        !exists ID #channel(Optional)
*/
```

