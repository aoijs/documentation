# $deleteMessage

This function deletes a message from the given message ID

#### Fields

This function has 2 fields

1. Channel ID \(Required\)
2. Message ID \(Required\)

Raw Usage: `$deleteMessage[messageID;channelID]`

#### Options

* Message ID - The message we're deleting
* Channel ID - The channel we're the message is

#### Usage

```javascript
bot.command({
name: "delete-me",
code: `Deleted the message!
$deleteMessage[$message;$channelID]
`
})
```

