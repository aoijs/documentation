---
description: >-
  An event that gets executed, if the bot sees a user reacting with a reaction
  to a message. To let the bot listen to the event, add one bot.onReactionAdd()
  callback inside your mainfile.
---

# bot.onReactionAdd

#### Usage:

```javascript
bot.reactionAddCommand({ //command
        channel: "channel id", //the channel where the bot will log
        code: `your code` //Message that will be sent to <channel>
})
```

#### Example Command:

```javascript
bot.reactionAddCommand({
        channel: "772414449839636490", 
        code: `$username has reacted with $emojiToString`
})
```

#### Functions:

* [$emojiToString](../functions/usdemojitostring.md) =&gt; the exactly emoji itself, either default emoji e.g. `🎉` or `<:emojiname:emojiID>` style. 
* [$emojiName ](../functions/usdemojiname.md)=&gt; the name of the emoji the user reacted with
* [$emojiID](../functions/usdemojiid.md) =&gt; the ID of the emoji the user react with \(for custom Emojis\)
* [$messageID](../functions/usdusermessageid.md) =&gt; to get the messageID the user reacted 
* $authorMessage =&gt; to get the authorID of the message the user reacted to 
* [$channelID ](../functions/usdchannelid.md)=&gt; to get the channelID of the message
* [$channelID ](../functions/usdchannelid.md)=&gt; to get the channelID of the message
* [$authorID](../functions/usdauthorid.md) =&gt; the ID of the user that reacted
* [$username](../functions/usdusername.md) =&gt; the username of the user that reacted

{% hint style="info" %}
You can use functions like [$onlyForChannels](../functions/usdonlyforchannels.md) or the functions from above in an[ $onlyIf\[\]](../functions/usdonlyif.md) limiter at the bottom of the code to limit your code to specific reactions etc.
{% endhint %}

