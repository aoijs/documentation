---
description: Updates the cache for the current guild members
---

# $cacheMembers

This function is responsible for saving each new user that has not been registered before in your bot's database.

### Usage 
```php
$cacheMembers[guildID?;returnCount?]
```

### Field
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guild ID |The guild we're caching the members for | number | no |
|return count|The amount of members cached|yes/no|no|

## Examples

- Without optional fields

```javascript
bot.command({
    name: "update",
    code: `
    Members cached.
    $cacheMembers
    `
});
```

- With optional fields

```javascript
bot.command({
    name: "update",
    code: `
    $cacheMembers[773352845738115102;yes] members cached.
    
    `
});
```

