# $loopStatus

This function will tell you the current loop status, if it's in song, the entire queue or none.

Statuses:
* none
* queue
* song

Example:

```javascript
bot.command({
    name: "loopstatus",
    code: `
    The current loop status is in $loopStatus
    `
})
```

