# $removeContains

This function will allow you to delete the amount of messages you specify which contain the word you request.

Raw usage: `$removeContains[channelID;limit;word1;word2;...]`

Example:

```javascript
bot.command({
    name: "purge-words",
    code: `Done!
    $removeContains[$channelID;$message[1];bald]
    `
});
```

This will delete the amount of messages specified in the message which contain the word "bald"

