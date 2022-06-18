---
description: Returns the server's highest role.
---
# $highestServerRole

This function returns the server's highest role.

### Usage
```php
$highestServerRole[guildID?;option?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The id of the guild | number | no |
| option | The option on basis of which the role will be returned | string | no |

#### Options
- `id` - Returns id of the role.
- `name` - Returns name of the role.
- `mention` - Returns the mention of the role.

## Example

```javascript
bot.command({
name: "role", 
code: `$serverName's Highest Role:
$highestServerRole`
})
```

