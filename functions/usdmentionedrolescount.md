# $mentionedRolesCount

With this function you can check how many channel mentions in the command's message are.

Raw usage: `$mentionedRolesCount`

#### Example Command:

```js
bot.command({
name: "rolementions",
code: `
You have $mentionedRolesCount role mentions in your message.`
});
```

