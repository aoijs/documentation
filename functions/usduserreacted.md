# $userReacted

This function will return `true` or `false` depending if the user reacted with given emoji to given message ID.

Raw usage: `$userReacted[messageID;userID;emoji]` or `$userReacted[channelID;messageID;userID;emoji]`

Example:

```javascript
bot.command({
    name: "reacted",
    code: `
    $userReacted[784626845059383316;808044141048627260;$authorID;<:checkmark:805116425345302528>]
    `
});

// This will check if the user reacted with the :checkmark: emoji to one of my tips.
```

