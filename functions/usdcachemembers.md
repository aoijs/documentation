---
description: Updates the cache for the current guild members
---

# $cacheMembers

This function is responsible for saving each new user that has not been registered before in your bot's database.

#### Fields

This function has 2 optional fields

1. Guild ID \(Optional\)
2. Return Count \(Optional\)

Raw Usage: `$cacheMembers[guildID (optional);returnCount (optional)]`

#### Options

* Guild ID - The guild we're caching the members for
* Return Count - The amount of members cached

#### Usage

Without optional fields

```javascript
bot.command({
    name: "update",
    code: `
    Members cached.
    $cacheMembers
    `
});
```

With optional fields

```javascript
bot.command({
    name: "update",
    code: `
    $cacheMembers[773352845738115102;yes] members cached.
    
    `
});
```

