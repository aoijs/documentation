---
description: Returns lowest role a user has in the server.
---
# $lowestRole

This function returns the lowest role a user has. This does NOT return @everyone.

### Usage
```php
$lowestRole[userID?;guildID?]
```

### Fields

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| user ID | The id of the user whose lowest role is to be found | number | no |
| guild ID | The id of the guild| number | no |

## Example

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

