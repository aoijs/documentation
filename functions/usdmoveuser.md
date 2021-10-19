# $moveUser

This function will make the bot move a user from the current voice channel to the selected voice chat using the channel ID or disconnect if Channel ID isn't specified.

This function has 3 fields:

1. User ID \(Required\)
2. Channel ID \(Optional\)
3. Reason \(Optional\)

Raw usage: `$moveUser[User ID;Channel ID (Optional);Reason (Optional)]`

Example:

```javascript
bot.command({
    name: "move",
    code: `
    Moved!
    $moveUser[278342221202194434;778626945209991170]
    `
})
```

