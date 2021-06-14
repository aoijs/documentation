# $messagePublish

This function will publish the message \(Only works in announcement channels\)

Raw usage: `$messagePublish[Channel ID (Optional);Message ID (Optional)]`

Example:

```javascript
bot.command({
    name: "publish",
    code: `
$messagePublish
Hello!
    `
})
/**
* With this the bot will send a message saying
* 'Hello!'
* And once the message was sent it will publish it
* Sending it to every server who follows that
* Announcements channel.
*/
```

