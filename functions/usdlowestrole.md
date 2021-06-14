# $lowestRole

This function returns the lowest role a user has. This does NOT return @everyone

```text
$lowestRole[userID (optional)]
```

```javascript
bot.command({
name: "role", 
code: `$username's lowest Role:
$lowestRole`
})
```

Lowest role for the mentioned user

```javascript
bot.command({
name: "role", 
code: `$username's lowest Role:
$lowestRole[$mentioned[1]]`
})
```

