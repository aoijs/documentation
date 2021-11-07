# $getBanReason

This function gets the reason of the ban for the specified user 

#### Fields

This function has 1 required field

1. User ID \(Required\)
2. Guild ID \(Optional\)

Raw Usage: `$getBanReason[userID;guildID (optional)]`

#### Options

* User ID - The user we're getting the reason for
* Guild ID - The guild we're the user was banned

#### Usage

Without optional field

```javascript
bot.command({
name: "banReason",
code: `$getBanReason[$mentioned[1]]`
})
```

With optional field

```javascript
bot.command({
name: "banReason",
code: `$getBanReason[$mentioned[1];773352845738115102]`
})
```

