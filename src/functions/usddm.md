---
description: DM a user ID.
---

# $dm

This function DMs the given user via ID

#### Fields

This function has 1 optional field

1. User ID \(Optional\)

Raw Usage: `$dm[userID (optional)]`

#### Options

* User ID - The user we're dming

#### Usage

DMing the author

```javascript
bot.command({
name: "dm", 
code: `
$dm Hello!` 
})
```

DMing the mentioned user

```javascript
bot.command({
name: "dm", 
code: `
$dm[$mentioned[1]] Hello!` 
})
```

