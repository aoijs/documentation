---
description: Returns the ID of the bot's owner.

---

# $botOwnerID

This function returns the ID\(s\) of the bot's owners.

## Fields

1. Separator \(Optional\)

#### Raw Usage: 
```php
$botOwnerID[separator (optional)
```

## Options

* Separator - The symbol/letter that separates the 2 or more ids \(if the bot has 2 or more owners\)

## Usage

```javascript
bot.command({
name: "botOwner",
code: `Here are my owners: $botOwnerID`
//Separator is for if your bot has multiple owners
})
```

