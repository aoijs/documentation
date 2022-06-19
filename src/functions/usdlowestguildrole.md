---
description: Returns the lowest role for the current/specified server.
---
# $lowestGuildRole

This function returns the lowest role for the current guild.

### Usage
```php
$lowestGuildRole[guildID?]
```


### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | Returns lowest server role for specific guild | number | no |

## Example

```javascript
bot.command({
name: "role", 
code: `$serverName's lowest Role: $lowestGuildRole`
})
```

