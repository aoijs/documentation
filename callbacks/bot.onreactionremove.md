---
description: >-
  An event that gets executed, if the bot sees a user removing a reaction on a
  message. To let the bot listen to the event, add one bot.onReactionRemove()
  callback inside your mainfile.
---

# bot.onReactionRemove

This callback logs _**every time**_ a user un-reacts to a message

#### Functions:

* [$emojiToString](../functions/usdemojitostring.md) =&gt; the exactly emoji itself, either default emoji e.g. `🎉` or `<:emojiname:emojiID>` style. 
* [$emojiName ](../functions/usdemojiname.md)=&gt; the name of the emoji the user unreacted with.
* [$emojiID](../functions/usdemojiid.md) =&gt; the ID of the emoji the user unreact with \(for custom Emojis\)
* [$messageID](../functions/usdusermessageid.md) =&gt; to get the messageID the user unreacted.
* $authorMessage =&gt; to get the authorID of the messagte the user unreacted to.
* [$channelID ](../functions/usdchannelid.md)=&gt; to get the channelID of the message
* [$authorID](../functions/usdauthorid.md) =&gt; the ID of the user that unreacted.
* [$username](../functions/usdusername.md) =&gt; the username of the user that unreacted

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

#### Command Handler Usage:
For people who use `bot.loadCommands()` handler.
```javascript
module.exports = ({
channel: "ID",
code: `
code here
`,
type: 'reactionRemoveCommand'
})
```
#### Example command:

```javascript
module.exports = ({
channel: "705681477169315863",
code: `$username has unreacted with $emojiToString`,
type: 'reactionRemoveCommand'
})
```

![Here&apos;s an example](../.gitbook/assets/image%20%2840%29.png)

{% hint style="info" %}
You can use functions like $onlyForChannels or the following functions inside an[ $onlyIf\[\]](../functions/usdonlyif.md) limiter at the bottom of the code to limit your code to specific reactions etc: 
{% endhint %}

