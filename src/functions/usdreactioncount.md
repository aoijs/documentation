---
description: Returns amount of people that have given a reaction to a certain message
---

# $reactionCount

This function will return the amount of people who reacted with given emoji to given message in the given channel.

The list of properties for this function are the next:

1. Channel ID.
2. Message ID.
3. Emoji.

```javascript
bot.command({
    name: "how-many",
    code: `
    $reactionCount[782007668831027201;804000541675749416;🎉] Users joined the giveaway in DBD.JS Official Server
    `
});
```

