# $sendMessage
> This function sends the &lt;message&gt; to the current channel

## Fields

## Usage
> ```
> $sendMessage[message;return message ID (yes/no)(required)]
> ```

```javascript
bot.command({
name: "sendMessage",
code: `$sendMessage[aoi.js is awesome;no]
//this will not send the message ID`
})
```

