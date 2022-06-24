---
description: >-
  An event that gets executed, if the bot sees a user removing a reaction on a
  message. To let the bot listen to the event, add one bot.onReactionRemove()
  callback inside your mainfile.
---

# bot.onReactionRemove

This callback logs _**every time**_ a user un-reacts to a message

#### Usage:

```javascript
bot.reactionRemoveCommand({ //command
channel: "channel id", //channel where it logs
code: `your code` // Message that will be sent to <channel>
}) 
```

#### Example Command:

```javascript
bot.reactionRemoveCommand({
channel: "772414449839636490", 
code: `
$username has unreacted with $emojiToString
`
}) 
```

![Here's an example](<../../.gitbook/assets/image (40).png>)

#### Functions:

* [$emojiToString](broken-reference) => the exactly emoji itself, either default emoji e.g. `🎉` or `<:emojiname:emojiID>` style.
* [$emojiName ](broken-reference)=> the name of the emoji the user reacted with
* [$emojiID](broken-reference) => the ID of the emoji the user react with (for custom Emojis)
* [$messageID](../functions/usdusermessageid.md) => to get the messageID the user reacted
* $authorMessage => to get the authorID of the messagte the user reacted to
* [$channelID ](../functions/usdchannelid.md)=> to get the channelID of the message
* [$authorID](../functions/usdauthorid.md) => the ID of the user that reacted
* [$username](../functions/usdusername.md) => the username of the user that reacted

{% hint style="info" %}
You can use functions like $onlyForChannels or the following functions inside an[ $onlyIf\[\]](../functions/usdonlyif.md) limiter at the bottom of the code to limit your code to specific reactions etc:
{% endhint %}
