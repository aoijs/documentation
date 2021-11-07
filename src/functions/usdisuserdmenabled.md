# $isUserDMEnabled

This function allows the bot tot check if the author/user's dms are enabled. Returns boolean

```text
$isUserDMEnabled[userID (optional)]
```

Using function

```javascript
bot.command({
    name: "userDMEnabled"
    code: `$isUserDMEnabled` //Checks for the author's dm
})
/* for someone else */
bot.command({
    name: "userDMEnabled"
    code: `$isUserDMEnabled[535566311942651924]` //Checks for Kubaturi/s dms
})
```

