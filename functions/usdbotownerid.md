# $botOwnerID

This function returns the ID\(s\) of the bot's owners

#### Fields

This function has 1 optional field

1. Separator \(Optional\)

Raw Usage: `$botOwnerID[separator (optional)`

#### Options

* Separator - The symbol/letter that separates the 2 or more ids \(if the bot has 2 or more owners\)

#### Usage

```javascript
bot.command({
name: "botOwner",
code: `Here are my owners: $botOwnerID`
//Separator is for if your bot has multiple owners
})
```

