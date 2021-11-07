# $deleteMessage

This function deletes a message from the given message ID

#### Fields

This function has 2 fields

1. Channel ID \(Required\)
2. Message ID \(Required\)

Raw Usage: `$deleteMessage[channelID;messageID]`

#### Options

* Channel ID - The channel we're the message is
* Message ID - The message we're deleting

#### Usage

```javascript
bot.command({
name: "deleteMessage",
code: `Deleted the message!
$deleteMessage[$channelID;800862561414414396]
`
})
```

