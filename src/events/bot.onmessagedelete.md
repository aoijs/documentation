# bot.onMessageDelete

This callback allows the bot to log any deleted message

```javascript
bot.deletedCommand({ //command
    channel: "channel id",
    code: `your code` //Message that will be sent to the channel
})
bot.onMessageDelete() //callback itself
```

Using the callback

```javascript
bot.deletedCommand({
    channel: "782446718704812032",
    code: `Message from $username, was deleted in <#$channelUsed>: $message`
    /*
        Code Breakdown
        $username - The user who wrote the message
        $channelUsed - The channel where the message was deleted
        $message - The message that was deleted
    */
})
bot.onMessageDelete()
```

