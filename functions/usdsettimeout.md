# $setTimeout

This function allows you to set a code to execute after given time. As extra, it won't stop if you reset the bot.

Raw usage: `$setTimeout[duration;timeout data;timeout heartbeat (optional)]`

Example:

```javascript
//Setting a timeout that will send a message to your dms after given time. 
bot.command({
    name: "remindme", 
    code: `You will be reminded with $messageSlice[1] after $message[1].
$setTimeout[$message[1];
userID: $authorID 
message: $messageSlice[1]]`
});

bot.timeoutCommand({
//    channel: "ID", (This is optional)
    code: `$sendDM[$timeoutData[userID];$timeoutData[message]]`
});
```

{% hint style="warning" %}
These can go above 21 days
{% endhint %}

This function also comes with a sub function called: `$timeoutData[property]` the property value will depend on what you add inside the second field of $setTimeout.

