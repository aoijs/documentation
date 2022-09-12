# $setTimeout

This function allows you to set a code to execute after given time. As extra, it won't stop if you reset the bot.

#### Usage

```
$setTimeout[name;duration;timeout data;returnId (optional);pulse (optional)]
```

#### Fields

This function has 2 required field

| Field | Description | Required |
| :--- | :--- | :--- |
| Name | Timeout name | Yes |
| Duration | Timeout duration | Yes |
| Timeout Data | Determines whether the timeout command should send pulse events to timeoutPulseCommands with the timeout data every X time until the timed data is deleted. | Yes |
| Return Id | Returns the Timeout ID | No |
| Pulse | Timeout Pulse | No |

## Examples

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

**These can go above 21 days**

This function also comes with a sub function called: `$timeoutData[property]` the property value will depend on what you add inside the second field of $setTimeout.

