# $getCustomStatus

This function returns the custom status of the given user, if they have one

```text
$getCustomStatus[userID (optional);state/emoji]
```

> ℹ️ state - The message, emoji - the emoji

```javascript
bot.command({
name:"customstatus",
code:`$getCustomStatus[502968724207304714;state]`
})
```

