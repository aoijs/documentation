# $mentionedUsersCount

With this function you can check how many user mentions in the command's message are.

Raw usage: `$mentionedUsersCount`

#### Example Commnd:

```js
bot.command({
name: "channelmentions",
code: `
You have mentioned $mentionedUsersCount users in your message.`
});
```

