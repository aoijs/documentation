# $botLastMessageChannelID

This function will return the ID of the channel where the last message of the bot was sent.

#### Usage

```javascript
bot.command({
    name: "id",
    code: `
My last message was sent in the channel <#$botLastMessageChannelID>
    `
})
```

