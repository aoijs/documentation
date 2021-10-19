# $mentionedChannelsCount

With this function you can check how many channel mentions are in the command's message.

Raw usage: `$mentionedChannelsCount`

#### Example Command:

```js
bot.command({
name: "channelmentions",
code: `
You have $mentionedChannelsCount channel mentions in your message.`
});
```

