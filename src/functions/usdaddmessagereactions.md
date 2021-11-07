---
description: Adds a reaction to the given message ID
---

# $addMessageReactions

This function will add a reaction to the specified message ID

#### Fields

This function has 3 required fields

1. Channel ID \(Required\)
2. Message ID \(Required\)
3. Reaction \(Required\)
4. Reaction 2 \(Optional\)
5. Etc

Raw usage: `$addMessageReactions[Channel ID;Message ID;Reaction 1;Reaction 2,...]`

#### Options

* Channel ID - The channel of which the &lt;messageID&gt; is situated in
* Message ID - The message of which the reactions will react to
* Reaction - The emojis of which will be reacted to the &lt;message&gt;

#### Usage

Singular Reaction

```javascript
bot.command({
    name: "react",
    code: `
    $addMessageReactions[$channelID;$messageID;🌸]
    Here's a pretty flower
    `
});
```

Multiple Reactions

```javascript
bot.command({
    name: "question",
    code: `
    $addMessageReactions[$channelID;$messageID;✔;❌]
    `
});
```

