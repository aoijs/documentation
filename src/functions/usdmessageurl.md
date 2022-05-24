---
description: Returns the message link to the author's message or specified message id.
---

# $messageURL

This function simply returns the message link to the command message or the provided message or channel id.

## Fields
- Message (Optional)
- Channel ID (Optional)

### Raw Usage
`$messageURL[messageID?;channelID?]`

## Options
- Message ID - The id of the author's message whose I'd is to be returned.
- Channel ID - The id of the channel from where the url of message is to be returned.

### Usage:

- Without optional fields:-

```js
bot.command({
name: "message-url",
code: `$messageURL`
})
```

- With optional fields:-

```js
bot.command({
name: "message-url",
code: `$messageURL[$channelID;$messageID]`
})
```



